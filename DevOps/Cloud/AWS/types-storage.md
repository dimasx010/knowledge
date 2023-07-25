# Types Storage

AWS storage services are grouped into three categories: block storage, file storage, and object storage.

## File storage

You may be familiar with file storage if you have interacted with file storage systems, such as Windows File Explorer or Finder on macOS. Files are organized in a tree hierarchy consisting of folders and subfolders. For example, if you have hundreds of cat pictures on your laptop, you may want to create a folder called "Cat Pictures" and place the images in that folder to organize them. Since you know that these images will be used in an application, you may want to place the Cat Pictures folder inside another folder called "Application Files".

Each file has metadata, such as the file name, file size, and the date the file was created. The file also has a path, for example, computer/Application_files/Cat_photos/cats-03.png. When you need to retrieve a file, the system can use the path to find it in the file hierarchy.

File storage is ideal when you need centralized access to files that multiple hosts need to easily share and manage. Typically, this storage is mounted on multiple hosts and requires file locking and integration into existing file system communication protocols.

Common use cases for file storage include the following:

- Large content repositories
- Development environments
- User home directories

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ab917891-c183-4d48-a074-e6ea0197b68a">
</p>

## Block storage

While file storage treats files as a singular unit, block storage divides files into fixed-sized chunks of data called "blocks" that have their own addresses. Because each block is addressable, blocks can be efficiently retrieved.

When data is requested, the storage system uses the addresses to arrange the blocks in the correct order to form a complete file for presentation to the requestor. Outside of the address, there is no additional metadata associated with each block. Therefore, when you want to change a character in a file, you simply change the block or fragment of the file that contains the character. This ease of access is why block storage solutions are fast and use less bandwidth.

Because block storage is optimized for low-latency operations, it is a typical storage choice for high-performance enterprise workloads, such as enterprise resource planning (ERP) systems or databases, which require low-latency storage.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b1d64541-de37-4b9c-badb-e066039935fe">
</p>


## Object storage

Objects, like files, are treated as a single unit of data when stored. However, unlike file storage, these objects are stored in a flat structure rather than in a hierarchy. Each object is a file with a unique identifier. This identifier, along with any additional metadata, is packaged with the data and stored.

Changing a single character in an object is more difficult than with block storage. When you want to change one character in a file, the entire file must be updated.

With object storage, you can store almost any type of data, and there is no limit to the number of objects stored, making it easily scalable. Object storage is often useful when storing large data sets; unstructured files, such as multimedia assets; and static resources, such as photos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2b3c9aa4-d401-4259-aabe-1a9a52357767">
</p>

