# SBT

```sbt
scalacOptions ++= Seq(
  "-source", "future" // "future-migration", "-rewrite"
, "-deprecation", "-nowarn", 
, "-language:strictEquality", "-language:postfixOps"
, "-Yexplicit-nulls"//, -language:unsafeNulls // (import scala.language.unsafeNulls)
, "release", "11"
, "-encoding", "UTF-8"
//, "-explain", "-explain-types"
)
```

```sbt
, scalacOptions ++=
    CrossVersion.partialVersion(scalaVersion.value) match {
      case Some((2, _)) => Nil
      case _ => Nil
    }
```

```sbt
turbo := true
useCoursier := true
Global / onChangedBuildSource := ReloadSourceChanges
```
