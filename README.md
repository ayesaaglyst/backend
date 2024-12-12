# **Nourish App - Backend API Documentation**

## **Authentication (Auth)**

### **Register**
- **Endpoint**: `/auth/register`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "name": "User 1",
    "email": "user1@gmail.com",
    "password": "password123"
  }

### **Login**
- **Endpoint**: `/auth/login`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "email": "user1@gmail.com",
    "password": "password123"
  }



## **Stories**

### **Create Stories**
- **Endpoint**: `/journal`
- **Method**: `POST`
- **Headers:**
  ```json
  {
      "Authorization": "Bearer <your_token>",
      "Content-Type": "multipart/form-data"
  }
- **Body (form-data):**


| Key         | Type     | Description                           |
|-------------|----------|---------------------------------------|
| `photo`     | File     | Gambar jurnal (wajib).               |
| `description` | String  | Deskripsi jurnal (wajib).            |
| `latitude`  | String   | Lokasi latitude (opsional).          |
| `longitude` | String   | Lokasi longitude (opsional).         |


### **Get Stories**
- **Endpoint**: `/journal`
- **Method**: `GET`
- **Query Parameters:**
  
| Parameter | Type   | Description                                            |
|-----------|--------|--------------------------------------------------------|
| `page`    | Number | Halaman data (default: 1).                             |
| `size`    | Number | Jumlah data per halaman (default: 10).                 |
| `location`| Number | `1` untuk hanya menampilkan data dengan lokasi (default: 0). |


### **Get Detail Story**
- **Endpoint**: `/journal/:journals_id`
- **Method**: `GET`


## **Nutrition**
- **Endpoint**: `/nutrition/classification`
- **Method**: `GET`
- **Query Parameters:**
  
- `classification` (required): The classification level to filter food recommendations. Valid values are:
  - `0` - Severely Stunted
  - `1` - Stunted
  - `2` - Normal
  - `3` - High

[Postman Url](https://drive.google.com/drive/folders/16HKeUbVj5d60eYlkc9oxulc6upzshpsr?usp=sharing) 

