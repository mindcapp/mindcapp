<div align="center">

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=560&lines=%3E+paqoe+--init;%3E+loading+kernel+modules...;%3E+starting+axolotl_daemon.service;%3E+status%3A+ACCEPTED" alt="Typing SVG" />
</a>

<p align="center">
  <img src="https://img.shields.io/badge/ROLE-SYSTEM__STAFF-1f242c?style=for-the-badge&logo=gnubash&logoColor=white&labelColor=30363d" />
  <img src="https://img.shields.io/badge/RUNTIME-GO__1.26-1f242c?style=for-the-badge&logo=go&logoColor=00ADD8&labelColor=30363d" />
  <img src="https://img.shields.io/badge/STATUS-ACCEPTED-238636?style=for-the-badge&labelColor=30363d" />
</p>

</div>

---

### `[0x00]` System Info // Neofetch Output

```text
    \  |  /        OS:         Darwin / Arch Linux (x86_64)
   ~( o.o )~       HOST:       mindcapp-core
    /  |  \        UPTIME:     while(alive) { run(); }
     d     b       CORE:       Go (goroutines & channels), net/http, slog
                   STORAGE:    PostgreSQL, Redis
                   TELEMETRY:  Prometheus, Grafana
                   DEPLOY:     Docker Compose, systemd, nginx, GitHub Actions
                   LOCATION:   Saint Petersburg
                   MASCOT:     axolotl // system_daemon.service [ACTIVE]
```

---

### `[0x01]` Microservice Runtime

```go
package main

import (
	"context"
	"log/slog"
)

type SystemStaff struct {
	Handle   string
	Role     string
	Stack    []string
	Accepted bool
}

func main() {
	ctx := context.Background()
	staff := &SystemStaff{
		Handle:   "paqoe",
		Role:     "Backend (Go) && InfoSec",
		Stack:    []string{"Go", "PostgreSQL", "Redis", "Docker", "Prometheus"},
		Accepted: true,
	}

	slog.InfoContext(ctx, "daemon started", "staff", staff.Handle, "status", "ACCEPTED")
	select {} // serve forever
}
```

---

### `[0x02]` Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=go,postgres,redis,docker,linux,prometheus,grafana,nginx,githubactions,bash,git&theme=dark" />
</p>

---

### `[0x03]` Projects

```text
$ ls -la ~/projects
drwxr-xr-x  song-vibes-check    Go · Redis · singleflight · Prometheus · CI/CD
drwxr-xr-x  attendance-bot      Go · Telegram · Docker · Grafana   [prod, 33 users]
drwxr-xr-x  kazakh-name-gen     Go · Gin · PostgreSQL · Prometheus
```

| Проект | Что делает | Стек |
| :-- | :-- | :-- |
| [**song-vibes-check**](https://github.com/mindcapp/song-vibes-check) | Сравнивает две песни по жанровым тегам MusicBrainz: Jaccard и взвешенная схожесть, объяснимый ответ, Redis-кэш с деградацией, лимит 1 req/s и повтор при 503 | Go, Redis, Prometheus, Grafana, GitHub Actions |
| [**attendance-bot**](https://github.com/mindcapp/attendance-bot) | Telegram-бот учёта посещаемости группы: явка, отчёты в чате и в Excel, напоминания, автодеплой на VPS | Go, Docker, Prometheus, Grafana, GitHub Actions |
| [**kazakh-name-generator**](https://github.com/mindcapp/kazakh-name-generator) | REST API генерации и хранения казахских имён с метриками и дашбордом | Go, Gin, PostgreSQL, Prometheus |

---

### `[0x04]` Request Trace // song-vibes-check

```zsh
$ trace POST /compare
[CACHE]    redis lookup ────────> HIT ──────────────> 200 OK   (~3 ms)
[MISS]     singleflight ────────> rate limit 1 rps ─> MusicBrainz
[SCORE]    normalize tags ──────> jaccard + weighted > 200 OK
[FAIL]     redis down ──────────> bypass cache ─────> still serving
```

---

### `[0x05]` Telemetry

<div align="center">

<img src="https://streak-stats.demolab.com?user=mindcapp&theme=tokyonight&hide_border=true&background=0D1117&ring=58A6FF&fire=7EE787&currStreakNum=58A6FF&sideNums=C9D1D9&sideLabels=C9D1D9&dates=8B949E" alt="GitHub Streak" />

</div>

---

### `[0x06]` Security Log

```text
$ cat /var/log/sec.log
[CTF]      ISPO CTF Cup ─────────> team lead (3 members)
[STUDY]    SPbSTU (ICST) ────────> ongoing
```

---

<div align="center">
  <sub>&gt; paqoe --help // contact: <a href="https://t.me/paqoe">t.me/paqoe</a></sub><br/>
  <sub>BUILD: RELEASE // Saint Petersburg, RU</sub>
</div>
