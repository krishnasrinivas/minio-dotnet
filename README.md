# Minio .NET Library for Amazon S3 Compatible Cloud Storage [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Minio/minio?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Install from NuGet [![Build Status](https://travis-ci.org/minio/minio-dotnet.svg?branch=master)](https://travis-ci.org/minio/minio-dotnet)

```powershell
To install Json.NET, run the following command in the Package Manager Console

PM> Install-Package Minio
```

## Example
```cs
using Minio;

private static MinioClient client = new MinioClient("https://s3-us-west-2.amazonaws.com", "Access Key", "Secret Key");

var buckets = client.ListBuckets();
foreach (Bucket bucket in buckets)
{
    Console.Out.WriteLine(bucket.Name + " " + bucket.CreationDate);
}

```

### Additional Examples

#### Bucket Operations
* [ListBuckets.cs](./Minio.Examples/ListBuckets.cs)
* [MakeBucket.cs](./Minio.Examples/MakeBucket.cs)
* [RemoveBucket.cs](./Minio.Examples/RemoveBucket.cs)
* [BucketExists.cs](./Minio.Examples/BucketExists.cs)
* [ListObjects.cs](./Minio.Examples/ListObjects.cs)
* [DropAllIncompleteUploads.cs](./Minio.Examples/DropAllIncompleteUploads.cs)

#### Object Operations
* [PutObject.cs](./Minio.Examples/PutObject.cs)
* [GetObject.cs](./Minio.Examples/GetObject.cs)
* [GetPartialObject.cs](./Minio.Examples/GetPartialObject.cs)
* [RemoveObject.cs](./Minio.Examples/RemoveObject.cs)
* [StatObject.cs](./Minio.Examples/StatObject.cs)
* [DropIncompleteUpload.cs](./Minio.Examples/DropIncompleteUpload.cs)

## Contribute

[Contributors Guide](./CONTRIBUTING.md)
