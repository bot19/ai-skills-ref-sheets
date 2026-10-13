# Get Full Stack — C# / .NET

Notes from **Get Full Stack**, a recurring ID4ME session series that walks through our C#/.NET backend services from a front-end engineer's point of view.

Each session starts as a Teams recording. Some sessions are later turned into a printable reference sheet made with the [explainer-sheet](../../../explainer-sheet/) skill. Others stay as a recording only.

## Sessions

| Week | Date | Topic | What's here |
| --- | --- | --- | --- |
| 1 | 28 Aug 2026 | Service walkthrough & fundamentals | Reference sheet [HTML](week-01-four-mental-models-v1.0.html) · [PDF](week-01-four-mental-models-v1.0.pdf) · [recording][w1] |
| 2 | 18 Sep 2026 | Build a basic API | [Recording][w2] only |
| 3 | 09 Oct 2026 | Stripe webhooks | [Recording][w3] only |

### Week 1: Four Mental Models

A tour of `id4me.user.service`, condensed into four questions to ask of any backend:

1. **Boundaries:** do we own this code, or do we only call it?
2. **Dependency direction:** which way do dependencies point?
3. **Lifetimes:** how long do things live, and who shares them?
4. **Errors:** how does a service say no?

### Week 2: Build a basic API

No notes yet. See the recording.

### Week 3: Stripe webhooks

How Stripe calls our registered endpoint when a payment event happens, and how the user service reacts. Covers:

- checking the Stripe signature on each request
- the events we handle, such as `checkout.session.completed`, `invoice.paid`, failed payments, subscription pause, resume, update and delete, and customer deleted
- using Stripe's time travel to trigger renewals during testing

## Conventions

- **File names:** `week-NN-topic`, plus `-vX.Y` on finished reference sheets.
- **Status:** a week with no `.html` or `.pdf` file has no reference sheet yet.
- **Recordings:** the links below are internal Teams links and need an ID4ME login.

[w1]: https://teams.microsoft.com/l/meetingrecap?driveId=b%21O3QMvdhXnku1b-m4xJtgIZnLxqihIBxMgYO1jjVGkDNHFPPcl0ZBT7g_dOWOJtie&driveItemId=01WTTJQ2YCKW2CRRE3X5FLU25GGBLEI5OS&sitePath=https%3A%2F%2Fid4me-my.sharepoint.com%2Fpersonal%2Ftony_id4me_me%2FDocuments%2FRecordings%2FGet+Full+Stack-20260828_152505-Meeting+Recording.mp4&fileUrl=https%3A%2F%2Fid4me-my.sharepoint.com%2Fpersonal%2Ftony_id4me_me%2FDocuments%2FRecordings%2FGet+Full+Stack-20260828_152505-Meeting+Recording.mp4&iCalUid=040000008200E00074C5B7101A82E00807EA081C28547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&masterICalUid=040000008200E00074C5B7101A82E0080000000028547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&threadId=19%3Ameeting_Y2Q2ZTBjZDEtM2UzOC00ZDNiLWE3MzAtZjIyMGZhZjU2Nzc5%40thread.v2&organizerId=77ff47f7-1351-469b-9dcc-22919288b755&tenantId=c0fa3167-1300-46c6-9738-7faacb3753a7&callId=39cb29ed-57c2-4cc7-91f6-58c64747cc57&threadType=meeting&meetingType=Recurring&subType=RecapSharingLink_RecapCore&recapType=RecordingAndTranscript
[w2]: https://teams.microsoft.com/l/meetingrecap?driveId=b%21O3QMvdhXnku1b-m4xJtgIZnLxqihIBxMgYO1jjVGkDNHFPPcl0ZBT7g_dOWOJtie&driveItemId=01WTTJQ2YJMHO7MWHH2JDJMRL5WTFQP3W3&sitePath=https%3A%2F%2Fid4me-my.sharepoint.com%2F%3Av%3A%2Fg%2Fpersonal%2Ftony_id4me_me%2FIQAJYd32WOfSRpZFfbTLB-7bAbJtJp13nHvOl9v6QQcYkTk&fileUrl=https%3A%2F%2Fid4me-my.sharepoint.com%2Fpersonal%2Ftony_id4me_me%2FDocuments%2FRecordings%2FGet+Full+Stack-20260918_145955-Meeting+Recording.mp4%3Fweb%3D1&iCalUid=040000008200E00074C5B7101A82E00807EA091228547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&masterICalUid=040000008200E00074C5B7101A82E0080000000028547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&threadId=19%3Ameeting_Y2Q2ZTBjZDEtM2UzOC00ZDNiLWE3MzAtZjIyMGZhZjU2Nzc5%40thread.v2&organizerId=77ff47f7-1351-469b-9dcc-22919288b755&tenantId=c0fa3167-1300-46c6-9738-7faacb3753a7&callId=39334987-c323-49fd-9a1b-a9274d45649e&threadType=meeting&meetingType=Recurring&subType=RecapSharingLink_RecapCore&recapType=RecordingAndTranscript
[w3]: https://teams.microsoft.com/l/meetingrecap?driveId=b%21O3QMvdhXnku1b-m4xJtgIZnLxqihIBxMgYO1jjVGkDNHFPPcl0ZBT7g_dOWOJtie&driveItemId=01WTTJQ26KUKNVGEPDORFL27MSR7234FP4&sitePath=https%3A%2F%2Fid4me-my.sharepoint.com%2F%3Av%3A%2Fg%2Fpersonal%2Ftony_id4me_me%2FIQDKoptTEeN0Sr19ko_1vhX8AfFVGr1PW0KJzPDpenDXmCA&fileUrl=https%3A%2F%2Fid4me-my.sharepoint.com%2Fpersonal%2Ftony_id4me_me%2FDocuments%2FRecordings%2FGet+Full+Stack-20261009_143540-Meeting+Recording.mp4%3Fweb%3D1&iCalUid=040000008200E00074C5B7101A82E00807EA0A0928547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&masterICalUid=040000008200E00074C5B7101A82E0080000000028547566C235DD010000000000000000100000002701C17627631144A6EA3205EFDB2F9F&threadId=19%3Ameeting_Y2Q2ZTBjZDEtM2UzOC00ZDNiLWE3MzAtZjIyMGZhZjU2Nzc5%40thread.v2&organizerId=77ff47f7-1351-469b-9dcc-22919288b755&tenantId=c0fa3167-1300-46c6-9738-7faacb3753a7&callId=0be17889-083c-4115-8ff9-a1f43c2d9560&threadType=meeting&meetingType=Recurring&subType=RecapSharingLink_RecapCore&recapType=RecordingAndTranscript
