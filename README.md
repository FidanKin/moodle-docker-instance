---

# Moodle Docker Taskfile 🐳🎓

This Taskfile helps you run **Moodle** in Docker.

Before using, make sure you have **Taskfile** installed: [https://taskfile.dev/docs/installation](https://taskfile.dev/docs/installation) ✅

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
