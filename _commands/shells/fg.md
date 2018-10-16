---
---

fg
--
Resume the specified job in the foreground, and make it the current job.
<!-- one line explanation would go here -->

<!-- minimal example --> 
~~~ bash
fg [job_id...]
~~~
<!--more-->

### Useful Options / Examples

Begin by running `jobs` to see which jobs are running in the background.
<!-- example --> 

~~~ bash
jobs
~~~

If you were to have a ping command running in the background, you might see something like this:

~~~ bash
[1]+  Running                 command ping -i 5 google.com &
~~~

The 1 indicates the job number. To bring this process to the **foreground**, we can refer to it by number like this:

~~~ bash
fg %1
~~~

If you leave the `job_id` field blank, fg will bring your most recently backgrounded process to the foreground

Once a job is in the foreground, you can kill it with CTRL-C, let it complete, or suspend and background it again.