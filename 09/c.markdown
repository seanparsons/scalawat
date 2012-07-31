Don't Block!
============

```scala
import akka.actor._
import akka.util.Timeout
import akka.util.duration._
import akka.pattern._

val actorSystem = ActorSystem("actorSystem")
case class ReplyActor() extends Actor {
  def receive = {
    case int: Int => {
      Thread.sleep(200)
      sender ! "Received Int: %s".format(int)
    }
    case _ => sender ! "Unknown received."
  }
}

val actorRef = actorSystem.actorOf(Props[ReplyActor], 
  name = "replyActor")
implicit val timeout = Timeout(5 seconds)
val future = actorRef ? 2000
future.onComplete{
  case Right(result) => println(result)
  case _ => println("Uh oh!")
}
actorSystem.shutdown()
```

