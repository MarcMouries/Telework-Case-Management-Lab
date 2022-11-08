---
layout: default
title: Introduction
has_children: true
nav_order: 1
permalink: /
has_toc: false
---

# Telework Case Management

## Introduction

Every organization is faced with the challenge of responding swiftly to the needs of its customers. It's easier said than done as most application development platforms require a steep learning before being productive. ServiceNow App Engine Studio takes away the complexity of building apps, so that more people can partipate and can focus on solving business problems instead of writing code.

## Goals

Our goals for this workshop are to allow you to:

1. Gain valuable experience through hands-on exercises with App Engine Studio
2. Convert a real-world use case with process bottlenecks to a streamline, cross enterprise workflow
3. Take back to your organization the knowledge of how you can make your world of work better.

[Next: Use-case](/docs/Part_0/Part_0.1_Use-case.md){: .btn-green-sn .btn }

<script>
    const navList = document.querySelector('.nav-list');
    let listItemToggleDarkMode = document.createElement("li");
    listItemToggleDarkMode.className = "nav-list-item";
    let anchorToggleDarkMode = document.createElement("a");
    anchorToggleDarkMode.className = "nav-list-link";
    anchorToggleDarkMode.href = '#';
    anchorToggleDarkMode.innerText = 'Light/Dark Mode';
    listItemToggleDarkMode.appendChild( anchorToggleDarkMode);
    navList.appendChild(listItemToggleDarkMode);

    jtd.addEvent(listItemToggleDarkMode, 'click', function(){
      if (jtd.getTheme() === 'dark') {
        jtd.setTheme('light');
       listItemToggleDarkMode.textContent = '🌙 Dark mode';
      } else {
        jtd.setTheme('dark');
        listItemToggleDarkMode.textContent = '☀️ Light mode';
      }
    });
</script>