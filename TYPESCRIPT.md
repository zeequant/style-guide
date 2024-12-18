# Typescript Guides

## Discriminated
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