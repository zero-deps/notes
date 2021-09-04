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
CrossVersion.partialVersion(scalaVersion.value) match {
  case Some((2, 13)) => opts
  case _ => opts
}
```

```sbt
turbo := true
useCoursier := true
Global / onChangedBuildSource := ReloadSourceChanges
```
