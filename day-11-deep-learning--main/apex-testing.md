# Apex Testing

## Overview

Apex Testing verifies that Apex code functions correctly and meets business requirements.

---

## Key Features

- Required for deployment
- Improves application reliability
- Validates business logic
- Supports continuous development

---

## Test Class Example

```apex
@isTest
private class AccountTest {

    @isTest
    static void testCreateAccount() {

        Account acc = new Account(
            Name = 'Test Account'
        );

        insert acc;

        System.assertEquals(
            'Test Account',
            acc.Name
        );
    }
}
```

---

## Important Annotations

### @isTest

Marks a class or method as a test.

```apex
@isTest
private class MyTestClass {
}
```

### Assertions

Used to verify expected outcomes.

```apex
System.assertEquals(
    expectedValue,
    actualValue
);
```

### Test.startTest() and Test.stopTest()

```apex
Test.startTest();

// Code under test

Test.stopTest();
```

---

## Best Practices

- Test positive and negative scenarios
- Use meaningful assertions
- Avoid hardcoded IDs
- Create reusable test data
- Keep tests independent

---

## Conclusion

Apex Testing ensures Salesforce applications remain reliable, maintainable, and deployment-ready.
