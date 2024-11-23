## `konserve-gcs`

```clojure
 litco/konserve-gcs
 {:git/url "https://github.com/The-Literal-Company/konserve-gcs.git"
  :git/sha "ba77feeda3b5506914708b675ca42f7eb36a966c"}
```

<hr>

### usage

+ `konserve-gcs/connect-bucket-store` will create buckets if they don't exist. 

+ Stores are a flat collection of blobs kept in folders. Deleting a store means deleting konserve blobs but ignoring the folder.

+ Optionally pass `:client` to override default service client.

```clojure
(require '[konserve-gcs.core :as kgcs])

(def spec
  {:bucket   "my-unique-bucket"
   :store-id "becomes-bucket-folder"
   :client   <provide-your-own-storage-instance>})
   
(def bucket-store (kgcs/connect-bucket-store spec :opts {:sync? true}))
```

### links
+ [konserve](https://github.com/replikativ/konserve)
+ [konserve-s3](https://github.com/replikativ/konserve-s3)
+ [konserve api walkthrough](https://github.com/replikativ/konserve/blob/main/doc/api-walkthrough.md)
+ [cloud.google.com/java/docs/reference/google-cloud-storage/latest](https://cloud.google.com/java/docs/reference/google-cloud-storage/latest/com.google.cloud.storage.Storage)
+ [cloud.google.com/java/docs/reference/google-cloud-storage/latest/com.google.cloud.storage.Bucket.Builder](https://cloud.google.com/java/docs/reference/google-cloud-storage/latest/com.google.cloud.storage.Bucket.Builder)
