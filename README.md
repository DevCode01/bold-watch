# Bold Watch

**Shell (Bash)** · **v0.1.0**

_Directory backup tool with timestamped archives_

---

## Features

- Creates timestamped .tar.gz archives
- Stores backups in ~/backups
- Reports archive size

## Installation

```bash
git clone https://github.com/DevCode01/bold-watch.git
cd bold-watch
```

## Usage

```bash
bash bold-watch.sh /path/to/dir
```

## How it works

Creates a timestamped gzip tar archive of a directory into `~/backups/`. The archive is named `<dirname>_<YYYYMMDD_HHMMSS>.tar.gz`, preserving the directory's basename inside the archive for clean restores.

## Options

- `dir` - directory to back up (default current directory)
- output archive goes to `~/backups/`

## Example

```bash
$ bash bold-watch.sh /path/to/dir
Backup created: /home/user/backups/dir_20260815_231031.tar.gz
Size: 4.0K
```

## Testing

```bash
bash tests/run.sh
```

Includes a functional check against real captured output, plus the build/syntax check.

## License

MIT
