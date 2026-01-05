
# Moodle Docker Taskfile 🐳🎓 #

This Taskfile helps you run **Moodle** in Docker.

Before using, make sure you have **Taskfile** installed: [https://taskfile.dev/docs/installation](https://taskfile.dev/docs/installation) ✅

This project is a simplified wrapper around the official [Moodle Docker](https://github.com/moodlehq/moodle-docker) repository, licensed under **GPL-3.0**.  

It removes unnecessary services and wraps everything in a Taskfile for one-command setup.
---

## Quick Start 🚀

```bash
git clone https://github.com/FidanKin/moodle-docker-instance.git .
task create-instance --m502l
```

Now you can open Moodle in your browser: [http://localhost:8000](http://localhost:8000) 🌐

---

## How It Works 🛠️

The Taskfile will create the specified directory (e.g., `task create-instance --m502l`, where `--m502l` is the directory name).
Inside this directory, there are two subdirectories:

* **mdocker** – contains only Docker files for Moodle. Source: [https://github.com/FidanKin/moodle-docker](https://github.com/FidanKin/moodle-docker) 🐳
* **www** – contains Moodle code files (version 5.0.2) 📂

After creating the directory, the script copies the config file from the Docker directory to the Moodle code directory. Then it runs `docker-compose`, and Moodle will be available in your browser at [http://localhost:8000](http://localhost:8000) 🎉

---

## Note ⚠️

You always need to run the Taskfile with an argument specifying the directory name.

## License

This project is licensed under [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html).  
Original Docker files are based on the official Moodle Docker repository.
