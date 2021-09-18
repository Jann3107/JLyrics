[![Stars](https://img.shields.io/github/stars/jagrosh/JLyrics.svg)](https://github.com/jagrosh/JLyrics/stargazers)
[![License](https://img.shields.io/github/license/jagrosh/JLyrics.svg)](https://github.com/jagrosh/JLyrics/blob/master/LICENSE)
[![CodeFactor](https://www.codefactor.io/repository/github/jagrosh/jlyrics/badge)](https://www.codefactor.io/repository/github/jagrosh/jlyrics)
[![Build status](https://ci.appveyor.com/api/projects/status/7gyee0nnox0y4756?svg=true)](https://ci.appveyor.com/project/jagrosh/jlyrics)

# JLyrics 
🎼 Expandable lyrics-scraping API for Java

# Info
Forked from jagrosh/JLyrics as they didnt update the Maven repo and Bintray shutdown.

## Example
```java
LyricsClient client = new LyricsClient();
Lyrics lyrics = client.getLyrics("smooth criminal").get();
System.out.println(lyrics.getContent()); // As he came into the window ...
```

## Features
  * Async or blocking (uses [CompletableFuture](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/CompletableFuture.html))
  * Built-in caching to prevent duplicate scrapes
  * Highly customizable (see [reference.conf](https://github.com/jann3107/JLyrics/blob/master/src/main/resources/reference.conf) and [lightbend/config](https://github.com/lightbend/config))
  * Easily expandable to many lyrics sites

## Included Lyrics Sites
  * A-Z Lyrics
  * Genius
  * MusixMatch

## Maven Setup
```xml
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
```

```xml
	<dependency>
	    <groupId>com.github.Jann3107</groupId>
	    <artifactId>JLyrics</artifactId>
	    <version>master-SNAPSHOT</version>
	</dependency>
```
