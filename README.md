### zerocell
---
https://github.com/creditdatamw/zerocell

```java
public class Person {
  @RowNumber
  private int rowNumber;
  
  @Column(index=0, name="FIRST_NAME")
  private String firstName;
  
  @Column(index=1, name="LAST_NAME")
  private String lastName;
  
  @Column(index=2, name="DATE_OF_BIRTH")
  private LocalDate dateOfBirth;
  
  public static void main(String... args) {
    List<Person> people = Render.of(Person.class)
      .from(new File("people.xlsx"))
      .sheet("Sheet 1")
      .list();
      
    String[] columns = Reader.columnOf(Person.class);
  }
}
pakcage com.example;

public class PersonReader implements ZeroCellReader {
}

package com.example;

@ZerocellReaderBuilder
public class Person {
  @RowNumber
  private int rowNumber;
  
  @Column(index=0, name="FIRST_NAME")
  private Strint firstName;
  
  
  
  
  
}
```

```
```

```
```


