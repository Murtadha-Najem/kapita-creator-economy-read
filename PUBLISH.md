# Publishing `iraq-creator-economy` on research.kapita.iq

Built 2026-09-30 12:37 (PREVIEW build: rebuild with --site before publishing).

1. Copy this folder to `kt-kapita-research-website/public/read-content/iraq-creator-economy/` (index.html and assets/).
2. `src/lib/standaloneReads.ts`: add `"iraq-creator-economy",` to STANDALONE_READS.
3. `src/app/(frontend)/read/staticReads.ts`: add this entry to `staticReads`:

```ts
  {
    id: "static-iraq-creator-economy",
    title: "تحويل التأثير إلى صناعة: صنّاع المحتوى العراقيون وعلاماتهم",
    description: "في العراق لم يعد المؤثر واجهة إعلانية، بل صار مؤسس علامة ومنافساً تجارياً مباشراً. قراءة تفاعلية في تقرير كابيتا البحثية عن صنّاع المحتوى وتطوير الأعمال.",
    slug: "iraq-creator-economy",
    status: "published",
    publishedAt: "2026-04-01T00:00:00.000Z",
    coverImage: { url: "/read-content/iraq-creator-economy/assets/img/cover.jpg", alt: "تحويل التأثير إلى صناعة: صنّاع المحتوى العراقيون وعلاماتهم", width: 1200, height: 900 },
  },
```

4. Check locally, then commit on a branch. A push to `main` deploys to production in about six minutes,
   so merge only on the owner's go.
5. After it is live: open https://research.kapita.iq/read/iraq-creator-economy , run verify.py against that URL,
   and ask whoever holds Search Console to request indexing.

Assets under /read-content are cached for a year; the site build names files by content hash, so a changed
image gets a new name automatically. Never overwrite a published asset under the same name.
