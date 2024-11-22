# Rules

#### Prefer chaining
```JS
  // Wrong
  const groupedOrders = _.groupBy(orders, (orderItem) => orderItem.transaction_id);
  const result = _.map(groupedOrders, (groupedOrders) => doSomething(groupedOrders));

  // Correct
  _.chain(orders)
    .groupBy((orderItem) => orderItem.transaction_id)
    .map((groupedOrders) => doSomething(groupedOrders))
    .value();
```

#### Prefer explicit methods 

Use utility methods that conveys your logic that writing the logic imperatively.

```JS
  const names = ['a', 'b', 'c'];
  const ids = [1, 2, 3];

  // Wrong
  _.map(names, (name, index) => {
    const id = ids[index];
    ...
  });
  // Correct
  _.map(_.zip(names, ids), [name, id] => {
    ...
  });
```

#### Conflicting objects:
```JS
	// Wrong:
	var superCategory = "fire"
	var superCategoryObject = _.find(CONFIG.***, ***)

	// Correct:
	var superCategoryName = "fire"
	var superCategoryConfig = _.find(CONFIG.***, ***)
```

#### Extracting Variables:
```JS
	// Wrong:
	var inputEmail = 'abc@abc.com'
	_.map(allowedEmails, (email) => { *** });

	// Correct
	var inputEmail = 'abc@abc.com'
	_.map(allowedEmails, (allowedEmail) => { *** });
```

#### Random variable names
```JS
  // Wrong
  temp = get_house_price_in_usd(house_sqft, house_room_count)
  final_value = temp * usd_to_aud_conversion_rate

  // Correct
  house_price_in_usd = get_house_price_in_usd(house_sqft, house_room_count)
  house_price_in_aud = house_price_in_usd * usd_to_aud_conversion_rate
```

```JS
  // Wrong
  temp = m1 * x1 + m2 * (x2 ** 2)
  final = temp + b

  // Correct
  house_price = price_per_room * rooms + price_per_floor_squared * (floors ** 2)
  house_price = house_price + expected_mean_house_price
```

#### Encourage truth variable names
```JS
	// Wrong
	if (isDisabled) { ....
	if (!isDisabled) { ...

	// Correct
	if(isEnabled) { ....
	if(!isEnabled) { ....
```