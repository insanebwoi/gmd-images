# gmd-images

Images for [getmydegreeedu](https://new.getmydegreeedu.com), served over the
jsDelivr CDN so the site's own repository stays small and the files cost the
site no bandwidth.

A file here is public at:

    https://cdn.jsdelivr.net/gh/insanebwoi/gmd-images@main/<path>

Blog covers are exactly 1400x787 WebP, which is 16:9. The site declares that
size through a `?w=&h=` suffix on the URL   jsDelivr ignores it, social cards
read it, and a preview renders before the image has been fetched. Keeping
every cover to one size is what lets that suffix be a single true number
rather than a per-file lookup.

Replacing a cover: commit the new file under the same name. jsDelivr caches
`@main` for up to 7 days, so either wait, purge it at
`https://purge.jsdelivr.net/gh/insanebwoi/gmd-images@main/<path>`, or commit
under a new filename and update the URL in the site's `postSchedule.ts`.
