---
layout: post
current: post
cover:  assets/images/rationality.jpeg
navigation: True
title: Why aren't we 100% rational?
date: 2022-07-16 10:00:00
tags: [CS]
class: post-template
subclass: 'post'
author: chenchik
---

What is concurrency? 

Для начала попытаемся понять какие проблемы у нас есть и после этого представим понятие concurrency

- Много ожидающих задач
- Нужно продолжать работу
- Придумали переключение потоков
- Потом придумали очереди, которые сами раскидываются на потоки
https://www.backblaze.com/blog/whats-the-diff-programs-processes-and-threads/#:~:text=Threads%20use%20the%20memory%20of,the%20process%20they%20belong%20to.
- Если использовать процессы - есть проблемка в синхронизации между ними и лишней памяти
- Если использовать треды - нужно копировать стэк
- mutex - токен, который дает возможность залочить от единого доступа 

Strictly speaking, two entities are run in parallel if at a given instant, both are currently executing.

However, two entities are concurrent if their execution lifetimes overlap.

The difference being that you can have concurrent threads on a uniprocessor and context switch between them, whereas in true parallelism you need at least two cores and the threads need to both be executing at the same time.

timesharing threads
