What's an actor?
================

```scala
import akka.actor._

val actorSystem = ActorSystem("actorSystem")
case class TestActor() extends Actor {
  def receive = {
    case "Kitteh" => println("Kitteh received, over and out.")
    case _ => println("Unknown received.")
  }
}

val actorRef = actorSystem.actorOf(Props[TestActor], 
  name = "testActor")
actorRef.tell("Kitteh")
actorRef ! "Dog"
actorSystem.shutdown()
```

Instances of actors are independent, only process one message at a time and queue said messages in a mailbox.
