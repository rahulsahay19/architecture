# Microservices Data Management

![image](https://user-images.githubusercontent.com/3886381/160231257-f8308150-0c06-4327-916d-1fe9e7bd24d1.png)

This section will address things like
- Data Duplication
- Polyglot consistency

## Best Practices
- Database per service pattern
- API Composition Pattern
- CQRS Pattern
- Event Sourcing Pattern
- Saga Pattern
- Shared Database anti pattern

![image](https://user-images.githubusercontent.com/3886381/160231467-1044818e-e251-4572-9565-2d29c8696bc8.png)

![image](https://user-images.githubusercontent.com/3886381/160231514-dafcd469-0300-4843-bf76-c024cffc2a0d.png)

![image](https://user-images.githubusercontent.com/3886381/160233167-b0b0cdda-ce23-47be-935c-9e8d9a72c57c.png)

![image](https://user-images.githubusercontent.com/3886381/160233202-20d85598-6a60-4d68-ba25-8cba60f98ab4.png)

Event sourcing pattern basically accumulates the events. It aggregates sequence of events into database. This way we can replay at certain point of events. This pattern is immensely used in CQRS and SAGA pattern.

![image](https://user-images.githubusercontent.com/3886381/160233316-b498920d-a3d9-49e8-be9c-fba01a980f48.png)

![image](https://user-images.githubusercontent.com/3886381/160233371-8c2b6eef-c40d-4dea-bd2e-23145c196d5a.png)

![image](https://user-images.githubusercontent.com/3886381/160233441-bbf57c4c-9d4b-4163-939a-a5ab001057ef.png)

![image](https://user-images.githubusercontent.com/3886381/160233477-b5a96a4a-f471-4e19-b1df-0b5237c326c2.png)

![image](https://user-images.githubusercontent.com/3886381/160233504-a100546f-ca5c-472e-ba91-b5a43fa422d3.png)

![image](https://user-images.githubusercontent.com/3886381/160233534-344599fe-0680-4936-a3a4-11c657bc14ac.png)

![image](https://user-images.githubusercontent.com/3886381/160233558-5683fcaa-904f-4104-91a3-2eb11a5318e5.png)

![image](https://user-images.githubusercontent.com/3886381/160233572-01be382c-7580-4756-bdc7-4489dec3e3d2.png)

![image](https://user-images.githubusercontent.com/3886381/160233625-f37ae1fe-cef3-4ce9-b3e6-d562b131dd39.png)

![image](https://user-images.githubusercontent.com/3886381/160233682-b935fbd2-94bc-4ac2-b685-35d6347e0837.png)

![image](https://user-images.githubusercontent.com/3886381/160233711-d1c4775c-9b5c-429e-b77d-c0f834724591.png)

![image](https://user-images.githubusercontent.com/3886381/160233797-937638d0-ee97-4f52-9c0f-d93dc49bd9e7.png)

![image](https://user-images.githubusercontent.com/3886381/160233815-83f27fcd-dcff-4885-aa29-7644f64bdaa0.png)

![image](https://user-images.githubusercontent.com/3886381/160233844-3bf39810-462d-4fc6-ae32-401d31b0ee3c.png)

![image](https://user-images.githubusercontent.com/3886381/160233873-1a814d47-fd67-47fd-a8ad-16bf50b233d9.png)

![image](https://user-images.githubusercontent.com/3886381/160233891-043d62fc-cc1f-43ce-a13b-3ff141691cdd.png)

![image](https://user-images.githubusercontent.com/3886381/160233913-849fead1-4132-4d64-ad37-98361b48be70.png)

![image](https://user-images.githubusercontent.com/3886381/160233936-91134f91-6cc1-4ef8-898a-27f656efd4d7.png)

![image](https://user-images.githubusercontent.com/3886381/160234022-25dc4801-c2c3-4155-88ab-0df90136959d.png)