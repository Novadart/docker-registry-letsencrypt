## Instructions

1. Checkout this repo and the submodule *docker-letsencrypt-nginx-proxy-companion*[1]
2. Replace *yourdomain.example.com* and *youremail@yourdomain.example.com* in the file `docker-compose.yml`
3. In the directory `registry-nginx` rename the file `yourdomain.example.com` using your domain name
4. Use the `htpasswd` tool to add your users in `registry.password`
5. Create the volume `docker-registry-data` using
    ```bash
        docker volume create docker-registry-data
    ```
    It will store the uploaded images
6. Run
    ```bash
        docker-compose up
    ```

[1] This submodule will not be necessary when [docker-letsencrypt-nginx-proxy-companion
](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion) will implement this PR: 
https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion/pull/203