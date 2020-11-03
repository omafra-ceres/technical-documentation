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

### `/user` Router

<details>
  <summary><code><strong>GET</strong> /user/users</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all users*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` userController.list
</details>

<details>
  <summary><code><strong>GET</strong> /user/datasets</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all datasets for the user making the request*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` userController.datasets
</details>

<details>
  <summary><code><strong>GET</strong> /user/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all archived (deleted) datasets for the user*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` userController.deleted
</details>

<details>
  <summary><code><strong>POST</strong> /user/create-dataset</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a dataset with the current user as owner*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` userController.createDataset
</details>

### `/admin` Router

<details>
  <summary><code><strong>GET</strong> /admin/users</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all users*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` adminController.users.list
</details>

<details>
  <summary><code><strong>GET</strong> /user/datasets</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a user with the provided info*
  
  &nbsp;&nbsp;&nbsp;&nbsp;`Action` adminController.users.create
</details>

## Controllers

### Data Controller Methods

#### `get()`
*Gets the details, items, and template for the requested dataset*

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>dataset</code></td>
      <td><strong>Object</td></strong>
      <td>Dataset details</td>
    </tr>
    <tr>
      <td><code>items</code></td>
      <td><strong>Array</td></strong>
      <td>Items associated with the dataset</td>
    </tr>
    <tr>
      <td><code>template</code></td>
      <td><strong>Object</td></strong>
      <td>The JSON Schema template that defines the dataset data</td>
    </tr>
    <tr>
      <td><code>hasDeleted</code></td>
      <td><strong>Boolean</td></strong>
      <td>Whether the dataset has deleted items</td>
    </tr>
  </table>
</details>

#### `add()`
*Adds an item to the specified dataset*

<details>
  <summary>Request body</summary>
  
  An object representing the item to be added to the dataset. Should match the JSON Schema provided in the dataset template.
</details>

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>item</code></td>
      <td><strong>Object</td></strong>
      <td>The item that has been added</td>
    </tr>
  </table>
</details>

#### `deleted()`
*Lists the deleted items in the specified dataset*

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>items</code></td>
      <td><strong>Array</td></strong>
      <td>A list of the deleted items</td>
    </tr>
  </table>
</details>

#### `deleteItems()`
*Delete the specified items from the dataset*

<details>
  <summary>Request body</summary>
  
  An array of item ids to be deleted from the dataset.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `recoverItems()`
*Recover the requested dataset items*

<details>
  <summary>Request body</summary>
  
  An array of item ids to be recovered.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `update()`
*Update dataset info and details*

<details>
  <summary>Request body</summary>
  
  An object representing the values to be updated.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `collaborators()`
*List of collaborators for the dataset*

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>collaborators</code></td>
      <td><strong>Array</td></strong>
      <td>A list of the dataset's collaborators with basic user details</td>
    </tr>
  </table>
</details>

#### `addCollaborator()`
*Add a collaborator to the dataset*

<details>
  <summary>Request body</summary>
  
  An array of user objects to be added as collaborators.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `removeCollaborator()`
*Remove a collaborator from the dataset*

<details>
  <summary>Request body</summary>
  
  An object with the user id to be removed. `{ id: USERID }`
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `recoverDataset()`
*Recover a deleted dataset*

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `archiveDataset()`
*Delete the requested dataset*

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

#### `listGlobal()`
*List of global datasets*

<details>
  <summary>Response</summary>
  
  Array of global datasets with basic dataset details
</details>

#### `createGlobal()`
*Create a global dataset*

<details>
  <summary>Request body</summary>
  
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>details</code></td>
      <td><strong>Object</td></strong>
      <td>The dataset details to be created</td>
    </tr>
    <tr>
      <td><code>template</code></td>
      <td><strong>Object</td></strong>
      <td>The JSON Schema template for the dataset to be created</td>
    </tr>
  </table>
</details>

<details>
  <summary>Response</summary>
  
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>id</code></td>
      <td><strong>String</td></strong>
      <td>The id of the created dataset</td>
    </tr>
  </table>
</details>

#### `getGlobalOptions()`
*The value of the first column for each item in the global dataset, to be used as options for other datasets*

<details>
  <summary>Response</summary>
  
  <table>
    <tr>
      <th>Key</th>
      <th>Type</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>ops</code></td>
      <td><strong>Array</td></strong>
      <td>List of global dataset first column values</td>
    </tr>
  </table>
</details>