# GSSE - GreyScript Script Extender

**GreyScript Script Extender (GSSE)** is a modular library designed to enhance and expand the existing scripting capabilities of the GreyScript framework. By providing a flexible and extensible architecture, GSSE enables developers to build more powerful and feature-rich scripts within the GreyScript ecosystem.

We welcome community involvement—**feel free to explore the code, suggest improvements, or make contributions**

A bundle with all of the scripts in one file is located inside the build folder.

## 📚 Documentation

<details>
<summary><strong>📦 Module: <code>Crypto</code></strong></summary>
<br>

<details>
<summary><strong><code>Crypto.b64encode(text)</code></strong></summary>
<br>

Encodes a string with base64.

#### **Parameters**
- `text` *(string)*: The string to be encoded with base64.

#### **Returns**
- *(string)*: The base64 encoded version of the text.

#### **Example**
```lua
b64encoded = Crypto.b64encode("Hello, World!")
print(b64encoded)
```
</details>

<details>
<summary><strong><code>Crypto.b64decode(text)</code></strong></summary>
<br>

Decodes a base64 encoded string.

#### **Parameters**
- `text` *(string)*: The base64 encoded string to be decoded.

#### **Returns**
- *(string)*: The plaintext version of the base64 encoded text.

#### **Example**
```lua
text = Crypto.b64decode("SGVsbG8sIFdvcmxkIQ==")
print(text)
```
</details>

<details>
<summary><strong><code>Crypto.sha256(text)</code></strong></summary>
<br>

Hashes a string with sha256.

#### **Parameters**
- `text` *(string)*: The string to be hashed.

#### **Returns**
- *(string)*: The sha256 version of the string.

#### **Example**
```lua
hash = Crypto.sha256("S3cure!")
print(hash)
```
</details>

<details>
<summary><strong><code>Crypto.aes128(choice, password, text)</code></strong></summary>
<br>

Encrypts or decrypts a string with aes128.

#### **Parameters**
- `choice` *(string)*: Choose between 'encrypt' or 'decrypt'.
  - `encrypt`: Encrypts the string.
  - `decrypt`: Decrypts the string.
- `password` *(string)*: The password used to encrypt the string.
- `text` *(string)*: The string to be encrypted or decrypted.

#### **Returns**
- *(string)*: The aes128 encrypted or decrypted version of the string.

#### **Example**
```lua
ciphertext = Crypto.aes128("encrypt", password, text)
decrypted = Crypto.aes128("decrypt", password, ciphertext)
print(decrypted)
```
</details>
</details>


<details>
<summary><strong>📦 Module: <code>files</code></strong></summary>
<br>


<details>
<summary><strong><code>getFile(object, path)</code></strong></summary>
<br>

Gets a file object from another object.

#### **Parameters**
- `object` *(object)*: This object is used to obtain the file object.
  - `file`: Gets a file object from another file object.
  - `computer`: Gets a file object from a computer object.
  - `ftpShell`: Gets a file object from an ftpShell object.
  - `shell`: Gets a file object from a shell object.
- `path` *(string)*: The path of the file object to obtain.

#### **Returns**
- *(object)*|*(null)*: The file object from the specified path or null on error.

#### **Example**
```lua
passwd_object = getFile(result, "/etc/passwd")
print(passwd_object.get_content)
```
</details>

<details>
<summary><strong><code>getUser(object)</code></strong></summary>
<br>

Returns the user that owns the object.

#### **Parameters**
- `object` *(object)*: This object is used to obtain the file object.
  - `file`: Gets a file object from another file object.
  - `computer`: Gets a file object from a computer object.
  - `ftpShell`: Gets a file object from an ftpShell object.
  - `shell`: Gets a file object from a shell object.

#### **Returns**
- *(string)*: The owner of the object.

#### **Example**
```lua
user = getUser(result)
print("The current user is: "+user)
```
</details>
</details>


<details>
<summary><strong>📦 Module: <code>Json</code></strong></summary>
<br>

<details>
<summary><strong><code>Json.dump(json)</code></strong></summary>
<br>

Converts the map into a json string

#### **Parameters**
- `json` *(map)*: The map to convert into a json string.

#### **Returns**
- *(string)*: The json string from the map.

#### **Example**
```lua
json_string = Json.dump({"key":"value"})
print(json_string)
```
</details>

<details>
<summary><strong><code>Json.loads(json)</code></strong></summary>
<br>

Converts the json string into a map

#### **Parameters**
- `json` *(string)*: The string to convert into a map.

#### **Returns**
- *(string)*: The map from the json string.

#### **Example**
```lua
json_map = Json.loads("{""key"":""value""}")
print(json_map)
```
</details>
</details>


<details>
<summary><strong>📦 Module: <code>lists</code></strong></summary>
<br>

<details>
<summary><strong><code>clean(myList)</code></strong></summary>
<br>

Removes empty strings from a list.

#### **Parameters**
- `myList` *(list)*: The that needs to be cleaned.

#### **Returns**
- *(list)*: The cleaned list.

#### **Example**
```lua
cleanList = myList.clean
cleanList = clean(myList)
print(cleanList)
```
</details>

</details>