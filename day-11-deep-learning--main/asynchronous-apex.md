# Asynchronous Apex

## Overview

Asynchronous Apex executes processes in the background, improving system performance and user experience.

---

## Benefits

- Faster user interactions
- Handles large datasets
- Supports long-running processes
- Improves scalability

---

## Types of Asynchronous Apex

### Future Methods

```apex
public class FutureExample {

    @future
    public static void processData() {
        System.debug('Future Method');
    }
}
```

---

### Queueable Apex

```apex
public class QueueableJob
implements Queueable {

    public void execute(
        QueueableContext context
    ) {
        System.debug('Queueable Job');
    }
}
```

Execute:

```apex
System.enqueueJob(
    new QueueableJob()
);
```

---

### Batch Apex

```apex
public class AccountBatch
implements Database.Batchable<SObject> {

    public Database.QueryLocator start(
        Database.BatchableContext bc
    ) {
        return Database.getQueryLocator(
            'SELECT Id FROM Account'
        );
    }

    public void execute(
        Database.BatchableContext bc,
        List<Account> scope
    ) {
        // Process records
    }

    public void finish(
        Database.BatchableContext bc
    ) {
        System.debug('Batch Complete');
    }
}
```

---

### Scheduled Apex

```apex
public class DailyJob
implements Schedulable {

    public void execute(
        SchedulableContext sc
    ) {
        System.debug('Scheduled Job');
    }
}
```

Schedule:

```apex
String cronExp =
'0 0 12 * * ?';

System.schedule(
    'Daily Job',
    cronExp,
    new DailyJob()
);
```

---

## Comparison

| Type | Use Case |
|--------|----------|
| Future | Simple background tasks |
| Queueable | Advanced asynchronous processing |
| Batch | Large-scale data processing |
| Scheduled | Time-based automation |

---

## Best Practices

- Prefer Queueable over Future methods
- Monitor Apex Jobs
- Handle exceptions properly
- Use Batch Apex for large datasets
- Schedule jobs responsibly

---

## Conclusion

Asynchronous Apex helps Salesforce applications perform efficiently by executing tasks in the background.
