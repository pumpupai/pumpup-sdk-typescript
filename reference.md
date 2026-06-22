# Reference
## Events
<details><summary><code>client.events.<a href="/src/api/resources/events/client/Client.ts">agentAction</a>({ ...params }) -> PumpUp.EventResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.events.agentAction({
    "Idempotency-Key": "Idempotency-Key",
    description: "Auto-classified claim as low-risk",
    projectName: "projectName",
    taskId: "taskId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.AgentActionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.events.<a href="/src/api/resources/events/client/Client.ts">exception</a>({ ...params }) -> PumpUp.EventResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.events.exception({
    "Idempotency-Key": "Idempotency-Key",
    message: "OCR failed on uploaded document",
    projectName: "projectName",
    taskId: "taskId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.ExceptionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.events.<a href="/src/api/resources/events/client/Client.ts">note</a>({ ...params }) -> PumpUp.EventResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.events.note({
    "Idempotency-Key": "Idempotency-Key",
    message: "Customer called to confirm bank details",
    projectName: "projectName",
    taskId: "taskId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.NoteRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Approvals
<details><summary><code>client.approvals.<a href="/src/api/resources/approvals/client/Client.ts">create</a>({ ...params }) -> PumpUp.EventResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns immediately with an event_id; poll the result endpoint by it for the decision.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.approvals.create({
    "Idempotency-Key": "Idempotency-Key",
    projectName: "claims_refund_v1",
    summary: "Refund $240 on claim C-1029",
    taskId: "taskId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.CreateApprovalRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ApprovalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.approvals.<a href="/src/api/resources/approvals/client/Client.ts">getResult</a>({ ...params }) -> PumpUp.ApprovalResult | undefined</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

200 with the outcome once a human has decided; 204 while still pending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.approvals.getResult({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.ApprovalsGetResultRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ApprovalsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Elicitations
<details><summary><code>client.elicitations.<a href="/src/api/resources/elicitations/client/Client.ts">create</a>({ ...params }) -> PumpUp.EventResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns immediately with an event_id; poll the result endpoint by it for the answers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.elicitations.create({
    "Idempotency-Key": "Idempotency-Key",
    fields: [{
            type: "DateField",
            id: "id",
            label: "label",
            required: true
        }],
    projectName: "projectName",
    summary: "Need additional details on the incident",
    taskId: "taskId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.CreateElicitationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ElicitationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.elicitations.<a href="/src/api/resources/elicitations/client/Client.ts">getResult</a>({ ...params }) -> PumpUp.ElicitationResult | undefined</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

200 with the provided fields once a human has answered; 204 while still pending.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.elicitations.getResult({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.ElicitationsGetResultRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ElicitationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Projects
<details><summary><code>client.projects.<a href="/src/api/resources/projects/client/Client.ts">list</a>({ ...params }) -> PumpUp.ProjectListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Optionally filter by a case-insensitive substring of the display name or slug; the response carries the slug to reference on ingest.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.projects.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.ProjectsListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProjectsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.projects.<a href="/src/api/resources/projects/client/Client.ts">get</a>({ ...params }) -> PumpUp.ProjectResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Includes the declared step graph.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.projects.get({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.ProjectsGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProjectsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tasks
<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">list</a>({ ...params }) -> PumpUp.TaskListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Optionally filter by projectId and/or a case-insensitive substring of the task name.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.list();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.TasksListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">create</a>({ ...params }) -> PumpUp.TaskResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The task opens in the project's initial state; use the returned id as taskId on subsequent events. The name is immutable.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.create({
    "Idempotency-Key": "Idempotency-Key",
    name: "Claim C-1029",
    projectName: "claims_refund_v1"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.CreateTaskRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">get</a>({ ...params }) -> PumpUp.TaskDetailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Materialized state — name, current state, metadata, attachments — plus open requests awaiting a human.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.get({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.TasksGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">events</a>({ ...params }) -> PumpUp.TaskEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Ascending cursor tail over the task's event log; pass nextCursor back as ?cursor= to resume. An absent cursor starts at the first event.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.events({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.TasksEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Uploads
<details><summary><code>client.uploads.<a href="/src/api/resources/uploads/client/Client.ts">upload</a>({ ...params }) -> PumpUp.UploadRef</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.uploads.upload({
    file: fs.createReadStream("/path/to/your/file")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.UploadRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UploadsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.uploads.<a href="/src/api/resources/uploads/client/Client.ts">get</a>({ ...params }) -> PumpUp.ResolvedUpload</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.uploads.get({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `PumpUp.UploadsGetRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UploadsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

