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
    
  public static void main(String... args) {
    File file = new File("people.xlsx");
    String sheet = "Sheet 1";
    ZeroCellReader<Person> reader = new com.example.PersonReader();
    List<Person> people = reader.read(file, sheet);
    people.forEach(person -> {
    });
  }  
}

public class Person {
  private int rowNo;
  
  private String id;
  
  private String firstName;
  
  private String middleName;
  
  private String lastName;
  
  private LocalDate dateOfBirth;
  
  private LocalDate dateOfRegistration;
  
  public static void main(String... args) {
    List<Person> people = Reader.of(Person.class)
      .from(new File("people.xlsx"))
      .using(
        new RowNumberInfo("rowNo", Integer.class),
        new ColumnInfo("ID", "id", 0, String.class),
        new ColumnInfo("FIRST_NAME", "firstName", 1, String.class),
        new ColumnInfo("MIDDLE_NAME", "middleName", 2, String.class),
        new ColumnInfo("LAST_NAME", "lastName", 3, String.class),
        new ColumnInfo("DATE_OF_BIRTH", "dateOfBirth", 4, LocalDate.class),
        new ColumnInfo("DATE_REGISTERED", "dateOfRegistration", 5, Date.class)
      )
      .sheet()
      .list();
    
    people.forEach(person -> {
      //
    });
  }
}
```

```
```

```
```


