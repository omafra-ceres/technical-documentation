# Ceres API documentation

Documentation for the Ceres RESTful API including routers, controllers, and services

## Routers

### `/data` Router

<br />

<details>
  <summary><code><strong>GET</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all data and details for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.get](#datacontrollerget)
  <br /><br />
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Edit details for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.update](#datacontrollerupdate)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `edit:details`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add item to a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.add](#datacontrolleradd)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `add:items`
  <br /><br />
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover an archived (deleted) dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.recoverDataset](#datacontrollerrecoverdataset)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `recover:dataset`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Archive (delete) a dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.archiveDataset](#datacontrollerarchivedataset)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `delete:dataset`
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get deleted items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.deleted](#datacontrollerdeleted)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `recover:items`
  <br /><br />
</details>

<details>
  <summary><code><strong>PUT</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover deleted items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.recoverItems](#datacontrollerrecoveritems)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `recover:items`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Delete items for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.deleteItems](#datacontrollerdeleteitems)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `delete:items`
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /data/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all collaborators for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.deleteItems](#datacontrollerdeleteitems)
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add a collaborator for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.addCollaborator](#datacontrolleraddcollaborator)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `update:collaborators`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/:datasetId/collaborators/delete</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Remove a collaborator for a specific dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.removeCollaborator](#datacontrollerremovecollaborator)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Scope</strong></code> `update:collaborators`
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /data/global</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all global datasets*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.listGlobal](#datacontrollerlistglobal)
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/global</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.createGlobal](#datacontrollercreateglobal)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>PUT</strong> /data/global/:datasetId</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Edit details for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.update](#datacontrollerupdate)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/collaborators</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Add a collaborator for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.addCollaborator](#datacontrolleraddcollaborator)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/collaborators/delete</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Remove a collaborator for a specific global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.removeCollaborator](#datacontrollerremovecollaborator)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>PUT</strong> /data/global/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Recover an archived (deleted) global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.recoverDataset](#datacontrollerrecoverdataset)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /data/global/:datasetId/archive</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Archive (delete) a global dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.archiveDataset](#datacontrollerarchivedataset)
  <br/>&nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Role</strong></code> `ADMIN`
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /data/global/:datasetId/options</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get all values from 1st column of the specific global dataset to be used as options in another dataset*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [dataController.getGlobalOptions](#datacontrollergetglobaloptions)
  <br /><br />
</details>

<br /><br />

### `/user` Router

<br />

<details>
  <summary><code><strong>GET</strong> /user/users</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all users*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [userController.list](#usercontrollerlist)
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /user/datasets</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all datasets for the user making the request*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [userController.datasets](#usercontrollerdatasets)
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /user/deleted</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all archived (deleted) datasets for the user*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [userController.deleted](#usercontrollerdeleted)
  <br /><br />
</details>

<details>
  <summary><code><strong>POST</strong> /user/create-dataset</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a dataset with the current user as owner*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [userController.createDataset](#usercontrollercreatedataset)
  <br /><br />
</details>

<br /><br />

### `/admin` Router

<br />

<details>
  <summary><code><strong>GET</strong> /admin/users</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Get a list of all users*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [adminController.users.list](#admincontrolleruserslist)
  <br /><br />
</details>

<details>
  <summary><code><strong>GET</strong> /user/datasets</code></summary><br />

  &nbsp;&nbsp;&nbsp;&nbsp;*Create a user with the provided info*
  
  &nbsp;&nbsp;&nbsp;&nbsp;<code><strong>Action</strong></code> [adminController.users.create](#admincontrolleruserscreate)
  <br /><br />
</details>

<br /><br />

## Controllers

### Data Controller Methods

#### `dataController.get()`
*Gets the details, items, and template for the requested dataset*

<details>
  <summary>Response</summary>
  <table>
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

<br />

#### `dataController.add()`
*Adds an item to the specified dataset*

<details>
  <summary>Request body</summary>
  
  An object representing the item to be added to the dataset. Should match the JSON Schema provided in the dataset template.
</details>

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <td><code>item</code></td>
      <td><strong>Object</td></strong>
      <td>The item that has been added</td>
    </tr>
  </table>
</details>

<br />

#### `dataController.deleted()`
*Lists the deleted items in the specified dataset*

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <td><code>items</code></td>
      <td><strong>Array</td></strong>
      <td>A list of the deleted items</td>
    </tr>
  </table>
</details>

<br />

#### `dataController.deleteItems()`
*Delete the specified items from the dataset*

<details>
  <summary>Request body</summary>
  
  An array of item ids to be deleted from the dataset.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.recoverItems()`
*Recover the requested dataset items*

<details>
  <summary>Request body</summary>
  
  An array of item ids to be recovered.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.update()`
*Update dataset info and details*

<details>
  <summary>Request body</summary>
  
  An object representing the values to be updated.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.collaborators()`
*List of collaborators for the dataset*

<details>
  <summary>Response</summary>
  <table>
    <tr>
      <td><code>collaborators</code></td>
      <td><strong>Array</td></strong>
      <td>A list of the dataset's collaborators with basic user details</td>
    </tr>
  </table>
</details>

<br />

#### `dataController.addCollaborator()`
*Add a collaborator to the dataset*

<details>
  <summary>Request body</summary>
  
  An array of user objects to be added as collaborators.
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.removeCollaborator()`
*Remove a collaborator from the dataset*

<details>
  <summary>Request body</summary>
  
  An object with the user id to be removed. `{ id: USERID }`
</details>

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.recoverDataset()`
*Recover a deleted dataset*

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.archiveDataset()`
*Delete the requested dataset*

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>

<br />

#### `dataController.listGlobal()`
*List of global datasets*

<details>
  <summary>Response</summary>
  
  Array of global datasets with basic dataset details
</details>

<br />

#### `dataController.createGlobal()`
*Create a global dataset*

<details>
  <summary>Request body</summary>
  
  <table>
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
      <td><code>id</code></td>
      <td><strong>String</td></strong>
      <td>The id of the created dataset</td>
    </tr>
  </table>
</details>

<br />

#### `dataController.getGlobalOptions()`
*The value of the first column for each item in the global dataset, to be used as options for other datasets*

<details>
  <summary>Response</summary>
  
  <table>
    <tr>
      <td><code>ops</code></td>
      <td><strong>Array</td></strong>
      <td>List of global dataset first column values</td>
    </tr>
  </table>
</details>

<br /><br />

### User Controller Methods

#### `userController.datasets()`
*List of a user's datasets*

<details>
  <summary>Response</summary>
  
  Array of datasets with basic dataset details
</details>

<br />

#### `userController.getDeleted()`
*List of a user's deleted datasets*

<details>
  <summary>Response</summary>
  
  Array of datasets with basic dataset details
</details>

<br />

#### `userController.createDataset()`
*Create a dataset for the logged in user*

<details>
  <summary>Request body</summary>
  
  <table>
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
      <td><code>id</code></td>
      <td><strong>String</td></strong>
      <td>The id of the created dataset</td>
    </tr>
  </table>
</details>

<br />

#### `userController.list()`
*List all users*

<details>
  <summary>Response</summary>
  
  Array of users
</details>

<br /><br />

### Admin Controller Methods

#### `adminController.users.list()`
*List all users*

<details>
  <summary>Response</summary>
  
  Array of users
</details>

<br />

#### `adminController.users.create()`
*Create a user with provided details*

<details>
  <summary>Response</summary>
  
  *Empty response on success*
</details>
