# 🏡 Second Brain — Home

> Selamat datang di Second Brain pribadi Ade Rizki.
> Tempat semua pengetahuan, ide, proyek, dan catatan terhubung.

---

## 📊 Quick Overview

```dataview
TABLE WITHOUT ID
  (length(rows)) AS "Total Notes"
FROM ""
WHERE file.name != "Home"
SORT length(rows) DESC
```

## 🎯 Active Projects

```dataview
TABLE
  status AS "Status",
  deadline AS "Deadline",
  priority AS "Priority"
FROM "03 - Projects"
WHERE status != "Completed"
SORT priority DESC, deadline ASC
```

## 📂 Quick Access

| Area | Deskripsi |
|------|-----------|
| [[01 - Home/Home\|🏡 Home]] | Halaman ini |
| [[07 - MOCs/_MOC Index\|🗺️ MOC Index]] | Semua Map of Content |
| [[08 - Inbox/Inbox\|📥 Inbox]] | Tangkapan cepat |
| [[02 - Daily Notes/\|📅 Daily Notes]] | Catatan harian |
| [[03 - Projects/\|🎯 Projects]] | Proyek aktif |
| [[04 - Areas/\|📋 Areas]] | Tanggung jawab & peran |
| [[05 - Resources/\|📚 Resources]] | Pengetahuan referensi |
| [[06 - Archives/\|🗄️ Archives]] | Arsip |

## 🧠 Recent Notes

```dataview
LIST
FROM ""
WHERE file.name != "Home"
SORT file.mtime DESC
LIMIT 10
```

## 🏷️ Tags Populer

```dataview
TABLE rows.file.link AS "Notes"
FROM -"00 - Meta"
FLATTEN file.tags AS tag
GROUP BY tag
SORT length(rows) DESC
LIMIT 10
```

---

*Last updated: {{date:YYYY-MM-DD}}*
