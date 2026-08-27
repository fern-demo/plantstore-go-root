# Reference
## plant
<details><summary><code>client.Plant.AddPlant(request) -> *plantstore.PlantResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.Plant{
    Name: plantstore.String(
        "Fern",
    ),
    Category: plantstore.String(
        "Indoor",
    ),
    Tags: []string{
        "green",
        "leafy",
    },
    Status: plantstore.PlantStatusAvailable.Ptr(),
}
client.Plant.AddPlant(
    context.TODO(),
    request,
)
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

**request:** `*plantstore.Plant` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Plant.UpdatePlant(request) -> *plantstore.PlantResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.Plant{
    Name: plantstore.String(
        "Fern",
    ),
    Category: plantstore.String(
        "Indoor",
    ),
    Tags: []string{
        "green",
        "leafy",
    },
    Status: plantstore.PlantStatusSold.Ptr(),
}
client.Plant.UpdatePlant(
    context.TODO(),
    request,
)
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

**request:** `*plantstore.Plant` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Plant.SearchPlantsByStatus() -> []*plantstore.PlantResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter plants based on their current status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.SearchPlantsByStatusRequest{}
client.Plant.SearchPlantsByStatus(
    context.TODO(),
    request,
)
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

**status:** `*plantstore.SearchPlantsByStatusRequestStatus` — The status of plants to search for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Plant.SearchPlantsByTags() -> []*plantstore.PlantResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter plants based on associated tags.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.SearchPlantsByTagsRequest{}
client.Plant.SearchPlantsByTags(
    context.TODO(),
    request,
)
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

**tags:** `*string` — Tags to filter plants (comma-separated).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Plant.GetPlantByID(PlantID) -> *plantstore.PlantResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a plant's details by its ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.GetPlantByIDRequest{
    PlantID: 1,
}
client.Plant.GetPlantByID(
    context.TODO(),
    request,
)
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

**plantID:** `int` — ID of the plant to retrieve
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## user
<details><summary><code>client.User.LoginUser() -> *plantstore.UserAuthResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.LoginUserRequest{}
client.User.LoginUser(
    context.TODO(),
    request,
)
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

**username:** `*string` — The username for login
    
</dd>
</dl>

<dl>
<dd>

**password:** `*string` — The password for login
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.User.LogoutUser() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.User.LogoutUser(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.User.GetUserByName(Username) -> *plantstore.User</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve user details using their username.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &plantstore.GetUserByNameRequest{
    Username: "username",
}
client.User.GetUserByName(
    context.TODO(),
    request,
)
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

**username:** `string` — Username of the user to retrieve
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

