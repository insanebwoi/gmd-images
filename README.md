# gmd-images

Images for [getmydegreeedu](https://new.getmydegreeedu.com), served over the
jsDelivr CDN so the site's own repository stays small and the files cost the
site no bandwidth.

A file here is public at:

    https://cdn.jsdelivr.net/gh/insanebwoi/gmd-images@main/<path>

Blog covers are 1400px wide WebP, cropped 16:9. The site declares them as
1600x900 through a `?w=&h=` suffix on the URL, which jsDelivr ignores and
social cards read, so a preview renders before the image is fetched.

Replacing a cover: commit the new file under the same name. jsDelivr caches
`@main` for up to 7 days, so either wait, purge it at
`https://purge.jsdelivr.net/gh/insanebwoi/gmd-images@main/<path>`, or commit
under a new filename and update the URL in the site's `postSchedule.ts`.
