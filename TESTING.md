# Testing 

- Avoid too much context. Test only the business logic.

## assert actual is equal to expected
```JS
describe('...', () => {
  it('...', () => {
    const creator = new Creator();
    const expected = {...};

    const actual = creator.create();

    // expect actual is equal to expected.
    expect(actual).to eql(expected);
  });

  // More concise test.
  it('...', () => {
    expect(new Creator().create()).to eql({
      ...
    });
  });
});
```

## Readability utils

```JS
  // WRONG
  assert(expected).to eql([
    { 
      datetime: '2024-01-01T10:00:01',
      tradingSymbol: new Instrument('TCS'),
      price: 100.0,
      volume: 2000,
      openInterest: 1045
    },
    {
      ...
    },
    {
      ...
    }
  ]);
  
  // CORRECT
  const flattenTick = (tick) => [
    tick.datetime,
    tick.tradingSymbol.toString(),
    tick.price,
    tick.volume,
    tick.openInterest
  ];
  assert(expected.map(flattenTick)).to eql([
    ['2024-01-01T10:00:01', 'TCS', 100.0, 2000, 1045],
    ['2024-01-01T10:00:02', 'TCS', 100.0, 2000, 1045],
    ['2024-01-01T10:00:03', 'TCS', 100.0, 2000, 1045],
    ['2024-01-01T10:00:04', 'TCS', 100.0, 2000, 1045],
    ['2024-01-01T10:00:05', 'TCS', 100.0, 2000, 1045],
  ]);
```