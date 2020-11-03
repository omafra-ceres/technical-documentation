# Ceres API documentation

Documentation for the Ceres RESTful API including routers, controllers, and services

## Routers

### `/data` Router

<details>
  <summary><code><strong>GET</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all data and details for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.get
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Edit details for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.update
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `edit:details`
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add item to a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.add
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `add:items`
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover an archived (deleted) dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.recoverDataset
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `recover:dataset`
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Archive (delete) a dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.archiveDataset
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `delete:dataset`
</details>

<details>
  <summary><code><strong>GET</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get deleted items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.deleted
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `recover:items`
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover deleted items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.recoverItems
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `recover:items`
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Delete items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.deleteItems
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `delete:items`
</details>

<details>
  <summary><code><strong>GET</strong> /data/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all collaborators for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.deleteItems
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add a collaborator for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.addCollaborator
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `update:collaborators`
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/collaborators/delete</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Remove a collaborator for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action:</strong></code> dataController.removeCollaborator
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope:</strong></code> `update:collaborators`
</details>

<details>
  <summary><code><strong>GET</strong> /data/global</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all global datasets*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.listGlobal
</details>

<details>
  <summary><code><strong>POST</strong> /data/global</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.createGlobal
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>PUT</strong> /data/global/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Edit details for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.update
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add a collaborator for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.addCollaborator
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/collaborators/delete</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Remove a collaborator for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.removeCollaborator
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>PUT</strong> /data/global/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover an archived (deleted) global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.recoverDataset
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Archive (delete) a global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.archiveDataset
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role:</strong></code> `ADMIN`
</details>

<details>
  <summary><code><strong>GET</strong> /data/global/:datasetId/options</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all values from 1st column of the specific global dataset to be used as options in another dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` dataController.getGlobalOptions
</details>
