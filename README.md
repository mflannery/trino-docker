trino-docker
# Running trino in podman / Docker

# First create a folder to hold the data catalog properties files in your local directory
mkdir -p ~/trino/catalog

# When selinux is running
```podman run -d -p 8080:8080 --volume ~/trino/catalog:/etc/trino/catalog:Z --name trino trinodb/trino```

# When selinux is disabled
```podman run -d -p 8080:8080 --volume ~/trino/catalog:/etc/trino/catalog --name trino trinodb/trino```
