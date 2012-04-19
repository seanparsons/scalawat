Implementing Unapply
====================

The unapply method is the crux of pattern matching, it's automatically created for case classes, but it's easy to make one yourself.

```scala
case class WebRequest(url: String, get: Boolean, params: Map[String, String])
case object GET {
  def unapply(webRequest: WebRequest): Option[String] = {
    if (webRequest.get) Option(webRequest.url) else None
  }
}

def parseGetRequest(webRequest: WebRequest): String = webRequest match {
  case GET(url) => "GET request for %s.".format(url)
  case _ => "Unknown"
}
println(parseGetRequest(WebRequest("/test", true, Map())))
// GET request for /test.
```

