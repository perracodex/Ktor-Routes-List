# Ktor-Routes-List
A [RouteCollector](https://github.com/perracolabs/Ktor-Routes-List/blob/main/RouteCollector.kt) example showing how to dump all registered routes in Ktor, including the corresponding HTTP method and path parameters.


Usage:

```kotlin
fun Application.module() {
    val endpoints: List<String> = this.collectRoutes()
    endpoints.forEach {
        println(it)
    }
}
```


Will produce results as next where each line is prefixed by the HTTP method, and path parameters are included when applicable

```console
GET /v1/employees
POST /v1/employees
DELETE /v1/employees
GET /v1/employees/{employee_id}
PUT /v1/employees/{employee_id}
DELETE /v1/employees/{employee_id}
POST /v1/employees/{employee_id}/employments
DELETE /v1/employees/{employee_id}/employments/{employment_id}
```
