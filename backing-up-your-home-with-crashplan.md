---
Title: Backing up your home with Crashplan
Date: 2016-11-14 08:44
Category: Tech
Tags: backup, crashplan
---

Backups are necessary today more than ever. You probably have a few gigs of photos on your phone, your music collection is digitised, you might have any amount of video content that you have *ahem* obtained from places, and all of it is liable to theft, disk failure or simple computer updates.

It's also a hard thing to think about. For most people a commercial cloud service may be enough. Most major digital retailers now provide backup for their products and you end up with your data scattered around - the things you buy from [Amazon][ed502868] or [Google Play][0c93493c] for example are stored by them (and not always that easy to get out). In addition there are any number of cloud storage providers who will offer free syncing with widely differing free tier packages - from [Dropbox's][60774993] 2Gb to [Mega's][6560c977] 50 - the subject of another piece I think.

However, if you're like me, you probably have more data than that. My current backup requirement is about a terabyte and growing. Again, most cloud services will provide a terabyte for a price, which has fallen to around £7 (which has been $10 for a long time, but with recent events I daren't look).

There are also cloud providers who will provide as much storage as you need on a per-unit basis. [Amazon S3][2b52d21a] is the most well known of these, along with their long term storage offering Glacier but there are others who also provide unlimited storage at generally competitive prices such as [Backblaze][d7c707ed].

A backup should ideally consist of two elements: a local one and an offsite one. My local backup goes to a cobbled together backup server made out of an Acer Revo which used to be my desktop machine, running Debian with a bunch of disks attached and mounted with [BTRFS][a43ccd51].

 After spending a few months trying to get backups working in a number of ways, which I will document one day, I seem to have settled on [Crashplan][ce6973fe]. They offer unlimited offsite backups per household with 2-10 computers for $13.99 a month or $149.50 a year ($12.50 a month). Their software also enables local backups and peer-to-peer backups for free. As a plan this is pretty impressive. If you have friends with spare capacity they can store your backups and you can store theirs.

  [ed502868]: https://www.amazon.co.uk//ref=as_li_ss_tl?ie=UTF8&linkCode=ll2&tag=eyetrails-21&linkId=d7161916ce86a30c2c9c087ef5061e95 "Amazon"
  [0c93493c]: https://play.google.com "Google Play"
  [60774993]: https://db.tt/fItgAqP4 "Dropbox"
  [6560c977]: https://mega.co.nz "Mega"
  [2b52d21a]: https://aws.amazon.com/s3/pricing/ "S3"
  [d7c707ed]: https://backblaze.com "Backblaze"
  [ce6973fe]: https://crashplan.com "Crashplan"
  [a43ccd51]: https://btrfs.wiki.kernel.org/index.php/Main_Page "BTRFS"
