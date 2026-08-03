# Revalidation: Time-based vs On-demand

Time-based revalidation (next: { revalidate: N }) refreshes cached data automatically after N seconds. On-demand revalidation (revalidatePath or revalidateTag, usually called from a Server Action or webhook after a content change) invalidates the cache immediately, precisely when you know data actually changed.

```javascript
import { revalidatePath } from "next/cache";

async function publishPost(id) {
  "use server";
  await db.posts.publish(id);
  revalidatePath(`/blog/${id}`);
}
```

**Key takeaway:** On-demand revalidation is strictly more precise than time-based - use it whenever you control the event that changes the data, such as a CMS webhook or your own mutation.
