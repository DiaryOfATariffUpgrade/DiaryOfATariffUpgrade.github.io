---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<script>
    function weeksAndDaysWithoutService() {
    	weeksAndDaysBetween(Date.parse("03 Jun 2024"), Date.parse("13 Aug 2024"));
    }
    
   	function daysSince(start) {
		writePlural(elapsedDays(start), "day");
   	}

   	function weeksAndDaysSince(start) {
	   	const startDate = Date.parse(start);   	
	   	weeksAndDaysBetween(startDate, Date.now());
   	}
   	
   	function weeksAndDaysBetween(startDate, endDate) {
   		const totalDays = elapsedDaysBetween(startDate, endDate);
   		const weeks = Math.floor(totalDays / 7);
   		const days = totalDays - 7 * weeks;
   		if (weeks != 0) {
   			writePlural(weeks, "week");
   			if (days != 0) {
				document.write(", ");
			}
		}
		if (days != 0) {
			writePlural(days, "day");
		}   	
   	}

   	function writePlural(count, unit) {
		document.write(`${count} ${unit}`);
		if (count != 1) {
			document.write("s");
		}
   	}
    
	function elapsedDays(start) {
	   	const startDate = Date.parse(start);
   		const now = Date.now();
   		return elapsedDaysBetween(startDate, now);
   	}

    function elapsedDaysBetween(startDate, endDate) {
   		return Math.floor((endDate - startDate) / 60 / 60 / 24 / 1000);    
    }

   	function daysSinceComplaint() {
   		daysSince("10 Jun 2024 GMT");
   	}
</script>

## TL;DR

On June 3rd I began the process of switching to a tariff with more data allowance, staying with the same network, keeping my old number of 20+ years. I have not had a working service since.

Ofcom states that porting a number from one network *to another* should take less than 24 hours and that compensation should be offered whenever that is not the case. I stayed with the *__same__* network, which feels like it should be a safer, quicker process.

<strike>So far, I have not had a working service for <b><script>weeksAndDaysSince("03 Jun 2024")</script></b>.</strike><br/>
**UPDATE**: As of August 13th, my service has finally seems to be working! Nobody from O2 has actually contacted me yet to announce/confirm this though, so maybe they're not done tweaking things...

All I want is my old number working as it did at the end of May, with a higher data allowance and a revised bill.

## Current Status

#### New SIM
Correctly identifies itself to my phone, with my number

#### Making calls
I can make a call from my phone, and the receiver sees it as coming from my number.

#### Receiving calls
Attempts to call my number fail to connect, resulting in an audio message such as:

 > "The number you have dialed has not been recognised"
 
 This is indicative that the network isn't even _trying_ to reach my phone, not that my phone itself is misconfigured. I have had to explain this multiple times.

#### Sending and receiving SMS messages
Neither works. Attempts to send a message result in the message being flagged as _"Not delivered"_ and _"Your message was not sent"_. In a world where so many online services (e.g. your bank) use SMS for two-factor authentication, this is problematic.

#### Facetime and iMessage
Both require SMS to authenticate a device, so I am not contactable via those services on my number.

#### Mobile data
Works fine

## Consequences

* Nobody with only my mobile number can contact me via voice calls, SMS, or by iMessage.
* To use any use service that requires SMS authentication, I have to jump through their security hoops to use a different method or to register an alternative number. To date that includes: two banks, an insurance provider, a pension provider and a payment service.
* I cannot register my phone for iMessage or Facetime as SMS authentication is **required**.
* I am paying for a second service for those times when being uncontactable is not an option.

## How did this happen?

On June 3rd I received the new SIM I had requested to move to an O2 rolling plan as I wanted more data than my current, years-old O2 monthly plan offered. Porting my original number over to that new plan didn't work. To address that, I was encouraged to switch to an un-publicised, discounted pay-monthly tarif, which I accepted.

<strike>Now, <b><script>weeksAndDaysWithoutService()</script></b> weeks later, I <i>still</i> do not have working service.</strike><br/>

This is despite:

 * Many calls to the helpline, totalling over 5 hours and including multiple unfulfilled promises of callbacks (3 promised, 1 received).
 
 * Opening an official complaint*, currently <script>weeksAndDaysSince("20 Jun 2024")</script> old. When/if it reaches 8 weeks old, on 15th August, Ofcom and the [Telecoms Ombudsman](https://www.commsombudsman.org) can get involved.

   *&nbsp; _"We aim to respond within 7 days"_
 
 * An email to the CEO - sent <script>weeksAndDaysSince("28 Jun 2024")</script> ago. No response so far.
 
 * A signed-for letter to the CEO - Signed-for <script>weeksAndDaysSince("04 Jul 2024")</script> ago. No response to date.
 
 * 3 "resolved" tickets, none of which has made any perceptible difference. (I expect the many helpdesk calls lead to other tickets being created, but I can only count the ones that have been explicitly identified to me. None have so far made any difference.)<br/>
 The _current_ active ticket was opened <script>daysSince("30 Jul 2024")</script> ago, and the last contact <script>daysSince("07 Aug 2024")</script> ago.
 
<B>NOTE</B>:<br/>
Everybody I have directly dealt with throughout this process has been polite, understanding and has _tried_ to be helpful - I have no complaint with them. However, that does not mean this process hasn't been *__incredibly__* frustrating. 

The problem seems to be that the mechanisms and processes of the inner workings of O2 serve as a barrier to resolution, not an as an enabler.

Porting a number between providers is [supposed to take less than 24 hours](https://www.ofcom.org.uk/phones-and-broadband/switching-provider/switching-mobile).

Surely staying with the same provider makes the process simpler?

Despite having an alternative contact number listed on my account, at no point has anybody with the knowledge and tools to fix this actually called me.

# The full history

### June

#### Monday 3rd
Rolling plan SIM activated

#### Tuesday 4th
Activation "completed", but phone still thinks it has the temporary number. Called support, promised a resolution within 24 hours.

#### Wednesday 5th
Still not working. Phoned support, persuaded that swtiching back to a (discounted) monthly tarif was the best path to resolution.

#### Thursday 6th
Pay-monthly SIM activation call - told to expect it to go live within 24 hours.

#### Friday 7th
Received an "order confirmation" SMS. My phone can make and receive calls, but doesn't know its own number so can't iMessage or FaceTime.

#### Saturday 8th, Sunday 9th
Tried all the recommended solutions - manually enter number, reset network settings, reboot phone, remove + replace SIM. Wait patiently without changing anything. No change.

#### Monday 10th
Another helpdesk call to report current status. No progress.

#### Tuesday 11th
A 42 minute call in which I immediately and repeatedly requested to speak to a supervisor (we're 4 failed calls in at this point, so escalation seemed reasonable), but I was repeatedly politely refused and deflected. A tech support ticket (#1) was raised and an update promised for the next day or Saturday.

#### Wednesday 12th
No callback

#### Saturday 15th
Still no callback

#### Monday 17th
Another helpdesk call, this time to be told that the previous ticket had been raised incorrectly (as an "email" ticket) and would have taken 10 days to process. An alternative "back office" ticket was raised in its place, with a promise of resolution within 4..24 hours (ticket #2).

#### Tuesday 18th
A confusing combination of events:
 * an SMS announcing that my number has been ported
 * a callback from yesterday's helpdesk operator telling me the number has been disconnected (I think they were accidentally referring to the SIM's original number?) and another callback was promised.
 
#### Wednesday 19th
No callback.

There's 3 ways of querying your account balance with O2:

 * Send an SMS to a particular number
 * Use the O2 app
 * Use your account on the O2 website
 
All 3 were giving me very different output, so I called the helpdesk to see about getting that untangled. After I explained the situation to him, and without any comment, the operative put me on hold. Eventually he returned, promising a fix within 24 hours.

That would be the last time I was able to send or receive a text (or for that matter, login to my O2 account, because it requires SMS authentication!).

#### Thursday 20th
I found the complaints email address ([complaintreviewservice@o2.com](mailto:complaintreviewservice@o2.com)) and sent the team there a message explaining my dissatisfaction. An automated reply was quickly sent out, claiming I should see a response within 7 days. (This was <script>weeksAndDaysSince("20 Jun 2024")</script> ago)

#### Saturday 22nd
Asked via Twitter to speak to somebody in the UK, but told the only option was the helpline.

#### Monday 24th
Another helpline call, totalling 54 minutes. Queries regarding the previously opened tickets were confusing, claiming the ticket wasn't opened until the 20th (was actually the 17th)

#### Tuesday 25th, Thursday 27th
Interactions over Twitter, containing assurances that the urgency of fixing this was being conveyed on tickets.

#### Friday 28th
Sent an email to the CEO ([lutz.schueler@virginmedia.co.uk](mailto:lutz.schueler@virginmedia.co.uk)) - no response to date.

Found some useful wording on the Ofcom website, albeit describing the process of moving a number _between_ providers:

> **Compensation if your switch is delayed**<br/>
> If the switch takes more than one working day or there is an abuse of the process by your provider, you are entitled to reasonable compensation from your provider. Providers must inform customers how to access this compensation and how it will be paid.

### July

#### Monday 1st
Called [Ofcom](https://www.ofcom.org.uk/make-a-complaint/complain-about-mobile-phone-or-internet-services/) for advice, and was told about the 8 week rule and the process of requesting a "dead-lock letter" and referring the issue to the [telecoms ombudsman](https://www.commsombudsman.org). I was also encouraged to contact the complaints address again, mentioning "ofcom".

#### Wednesday 3rd
Sent the CEO a signed-for letter, requesting my problem be given more attention. (Thanks to [ceoemail.com](https://www.ceoemail.com/s.php?id=ceo-9614&c=O2-Chief%20Executive) for providing the details)

#### Thursday 4th
Letter delivered, with an undecipherable "signature". Nothing has arisen from this.
Another email to the complaints address, referencing my original complaint and mentioning "ofcom" and "ombudsman", but again, it has had no discernable effect.

#### Friday 5th
Discovered the ["Resolver"](https://www.resolver.co.uk) service and used it to register a complaint, but was disappointed to find it seems to be nothing more than a web interface to the email address I'd already used.

<p style="font-family: monospace">&lt; No updates for a while as I was away &gt;</p>

<B>NOTE</B>:<br/>
From this point onwards all interactions have been via Twitter (generally DMs), unless otherwise stated.

#### Tuesday 23rd
Enquired about progress (actually sent the message yesterday, but after 5pm so fair enough). Had to explain the whole situation from scratch, again.

#### Wednesday 24th
Another ticket has been created (ticket #3) and a promise made that I will be updated.

#### Tuesday 30th
Almost another week has gone by - surely progress has been made?

Two prongs of attack today:

 * I emailed the complaints service again, pointing out that I do not consider the complaint resolved and that it has been 40 days since the last contact. (<script>daysSince("30 Jul 2024")</script> later and still no response)

 * Enquired about the progress of last Wednesday's ticket only to be told it has been closed. __*Another*__ new ticket is opened and escalated (ticket #4).
 
#### Wednesday 31st
For the first time I am provided with an update without having to ask for it. Sadly that update is disappointing in two ways:

 * It is announcing that the ticket has been resolved (and yet still my phone is unusable)

 * It is actually referring to the Wednesday 24th ticket (ticket #3), which we already knew was closed.
 
Given assurances that the current ticket is __*definitely*__ with the right team.

### August

#### Monday 5th
Enquired as to the progress of the latest ticket (#4), noting that I have not yet been called.

(2.5 hours later) For the first time in this process somebody from an internal team has reached out to me by email - maybe we're about to make meaningful progress?

#### Wednesday 7th
Disappointed not to have had any sort of progress report, I enquired whether any additional information was required and was told *"They will be in contact shortly once they have a response (from the support team)"*

#### Monday 12th
As "shortly" has well and truly expired, I requested an update (by email) as to the progress made since last Monday. The response was _"we'll let you know"_, so I replied requesting some urgency as today marks the 10 week point.

#### Tuesday 13th
My phone randomly popped up a "Do you want to use this number for Facetime?" alert, which prompted me to try ringing my number from another phone. And it worked! I sent an SMS and got a reply too! No actual update from O2 themselves yet, so keeping my fingers crossed and waiting to see what they have to say.

#### Wednesday 14th
Requested refund for undelivered service. Arranged for 6 months of Disney+ (always part of the deal, but the ability to choose it lapsed while I had no access to m account).
Suggested they might like to make a goodwill gesture to reflect the awful experience, inconvenience and was told that the refund was all the "compensation" they (the social media team) could provide. They did suggest I could raise an official complaint...

#### Thursday 29th
Wrote a physical letter to the complaints department this time (harder to ignore?) and sent it signed-for. Explained the 10 weeks, the effort required, the expense incurred and included all of the Twitter chat, as well as this diary. Total 17 pages.
Set a date in the calendar 8 weeks from now, expecting to have to go down the "dead-lock" letter + ombudsman route.

#### Friday 30th
Received an SMS saying:

> Unfortunately, we never heard back from you when we followed up on the issue you reported (ticket #4), so we've now had to close this request down. Please get back in touch if you still need help.

They made contact via email, which I did respond to. There was a back-and-forth, so they absolutely *do* know that I responded. Did they try to make contact via text, while SMS was broken? 🥴

A query from me (via email) yielded the response:

> Having reviewed the case from <person>, you’re correct.
> It appears to have been an oversight on their behalf.
> There is nothing new/outstanding on any other reference numbers.
> 
> Apoloigies for any inconvenience it caused.

Also, the signed-for complaint was "signed" for, by "Percy". Based on previous experiences with the complaints department (i.e. no response what-so-ever), I expect to be requesting a "dead-lock" letter on 23rd October. Presumably if *that* request is ignored, I can write to Ofcom directly?
