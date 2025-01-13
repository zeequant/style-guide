# Typescript Guides

## Types folder structure:
If the types are required everywhere put them in 
- src/types.ts
- src/types/domain.ts
- src/types/order.ts

If the types are required only in a single folder, put the types file or directory in that folder itself.


## All types/interfaces/enums should be in pascal case.

```TS
  // Wrong
  type MODIFYORDER = string;
  type productType = string;

  // Correct
  type ModifyOrder = string;
  type ProductType = string;
```

## Prefer narrow string unions rather than string type
```TS
  // Wrong
  interface Config {
    showShow: string;
  }

  // Correct
  interface Config {
    showShow: 'true' | 'false';
  }
```

## Prefer Enums instead of constants
```TS
  // Wrong
  const orderType: Record<string, string> = {
    'MARKET': 'MARKET',
    'SL': 'SL'
  };

  // Correct
  enum orderType = {
    MARKET = 'MARKET';
    SL =  'SL';
  }
```

## Prefer Discriminated Union
```
    interface HeaderSection {
      type: 'header';
      title: string;
    }
    interface TableSection {
      type: 'table';
      columns: string[];
    }
    interface FooterSection {
      type: 'footer';  
      links: string[];
    }
    type Section = HeaderSection | TableSection | FooterSection;

    function renderSection(section: Section) {
      switch (section.type) {
        case 'header':
          return <h1>{section.title}</h1>;
        case 'table':
          return <table>{section.columns.map(column => <th>{column}</th>)}</table>;
        case 'footer':
          return <footer>{section.links.map(link => <a href={link}>{link}</a>)}</footer>;
      }
    }
```

## Handling Date Strings

https://blog.logrocket.com/handling-date-strings-typescript/

```
  Branding utility to differentiate string types
  type Brand<K, T> = K & { __brand: T };

  export type YYYYMMDDString = Brand<string, 'YMDString'>;
  export type HHMMSString = Brand<string, 'HMSString'>;
```