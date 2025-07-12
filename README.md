### Here is how we delete all caches of a project :
```sh
cd /root/StudioProjects/Ricky/
./gradlew --stop
rm -rf .gradle
rm -rf */build
rm -rf build
./gradlew clean
```
### Rebuild the project
```sh
./gradlew assembleDebug
```
### -1 Create a file named KtorClient in (/network)

```sh
package com.farouk.network

import io.ktor.client.HttpClient
import io.ktor.client.engine.okhttp.OkHttp
import io.ktor.client.plugins.defaultRequest

    class KtorClient {
        private val client = HttpClient(OkHttp){
        defaultRequest { url("https://rickandmortyapi.com/api/") }
    }
}
```