---
title: How Code Buddy Works
layout: home
nav_order: 3
---

# How Code Buddy Works

The aim of this article is to give you a deeper understanding of how Code Buddy works under the hood so you can use it most effectively for your projects.

## Table of contents

- [Information Gathering](#information-gathering)
- [Data Processing](#data-processing)
- [Working with Full Code](#working-with-full-code)
- [Class Inclusion Rules](#class-inclusion-rules)
- [Conclusion](#conclusion)

## Information Gathering

To provide project information, Code Buddy collects a list of all public members of classes, structs, and interfaces in your project, along with their comments, and sends them as the first message at the start of each chat.

For example, if your code looks like this:

```csharp
/// <summary>
/// Manages game state, tracking enemy hits and time since the game started.
/// </summary>
public class GameManager : MonoBehaviour
{
    // The number of hits on the enemy.
    public int EnemyHits { get; private set; }

    // The time elapsed since the game started.
    public float TimeSinceStart { get; private set; }

    private void Start()
    {
        EnemyHits = 0;
        TimeSinceStart = 0f;
    }

    private void Update()
    {
        TimeSinceStart += Time.deltaTime;
    }

    /// <summary>
    /// Increments the enemy hit count.
    /// </summary>
    public void RegisterEnemyHit()
    {
        EnemyHits++;
    }
}
```

Then the context will look like this:

```txt
Class: GameManager : MonoBehaviour
Description: Manages game state, tracking enemy hits and time since the game started.

Properties:
- EnemyHits : int - The number of hits on the enemy.
- TimeSinceStart : float - The time elapsed since the game started.

Methods:
- RegisterEnemyHit() : void - Increments the enemy hit count.
```

To gather all this information, Buddy uses a combination of reflection and source file parsing. This approach minimizes context size, speed of executions, and significantly reduces request costs while providing all the necessary details for generating new code. Essentially, this process mirrors how a developer writes code manually, relying only on the public interface.

## Data Processing

If you need Code Buddy to work with full code, you can always attach a source code file to the chat. In the current version, virtual and protected methods of classes are not included in the context. So, if you want to generate a class extension, don’t forget to attach the base class files to the chat.

## Working with Full Code

It’s important to remember that the project context is gathered once at the start of each conversation. Therefore, it is recommended to start a new chat for generating each new class. Comments are also crucial for Code Buddy—they help it better utilize existing classes and methods, especially when similar names are present.

## Class Inclusion Rules

A special note should be made about class inclusion rules in the project context. By default, Code Buddy ignores everything located in Editor folders. This is done to keep the context clean and prevent confusion. However, if you are working on an editor extension, don’t forget to enable this option in the settings.

## Conclusion

I hope this information helps you better understand how Code Buddy works and how to use it more effectively. If you have any questions or need additional help, feel free to reach out to me on the [discord server](https://discord.gg/JdsepFhEeX).

Happy coding!
