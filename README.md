This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

<br/>

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

<br/>

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

<br/>

# Packages

- Shadcn
- Clerk
- Neon
- Drizzle
- zod
- use-server [Library throws an error if code ends up anywhere that's not on the server "Extra safety factor"]
- google calendar
- date-fns
- date-fns-tz

<br/>

# Code Exampling 

- singleEvents: true:
    - Anytime you have a reoccurring event like something that happens every Monday. Instead of returning just one instance it's going to every single instance in our range of dates

```bash
google.calendar('v3').events.list({
	calendarId: 'primary',
	eventTypes: ['default'],
	singleEvents: true,
	timeMin: start.toISOString(),
	timeMax: end.toISOString(),
	maxResults: 2500,
	auth: oAuthClient,
});
```
<br/>

- Using !== shows event if there is no schedule
- When going to schedule events and putting in the times it will work as intended

```bash
if (validTimes.length === 0) {
	return <NoTimeSlots event={event} calendarUser={calendarUser} />;
}
```