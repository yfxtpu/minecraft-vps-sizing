# Minecraft VPS Hosting: How to Size a Server by Single-Core Speed and Player Location

A Minecraft server's tick rate is decided by one CPU core and by the network path between that core and your players. Everything else on the spec sheet — vCPU count, disk size, the number of zeros in the traffic allowance — matters far less than those two things. GoMami sells Asia-Pacific VPS with routing optimised for mainland China, from $29/month for a 2-core/2GB box up to $599/month for a 56-core machine. Whether that's the right purchase depends almost entirely on where your players log in from and how heavy your world is.

> **Quick pick:** for a small Paper or lightly-modded server with players in Asia, the **JPN Pulse Mini at $49/month** (2 vCPU, 4GB RAM, 60GB NVMe, 1TB outbound on a 1.5Gbps port) is the sane starting point. Go bigger only for heavy modpacks or multiple worlds.
> 👉 [Check the JPN Pulse Mini at $49/month](https://bit.ly/Gomami)

## Do you actually need a VPS, or a Minecraft-specific host?

You need a VPS if shared game hosting has already failed you: TPS that collapses at 8pm, a panel that won't let you touch JVM flags, a node with forty customers on it. You don't need one if you want to click "create server", pick a modpack from a list, and never open a terminal.

The division of labour is concrete. A VPS gives you an empty Linux box with root access. You install Java, choose Paper or Fabric or NeoForge, open TCP 25565 for Java players and UDP 19132 for Bedrock (or add Geyser so both share one world), and wrap the process in systemd so it comes back after a reboot. A Minecraft-specific host does all of that for you.

GoMami sits on the VPS side, and its documentation says so plainly: you pick a node, pick a plan, choose a billing cycle, pay, and the VM deploys automatically within a few minutes with the IP and credentials arriving by email. No modpack installer, no "start server" button. If that reads like homework, the honest advice is to buy a managed Minecraft host and stop reading.

## The plans, node by node

The catalogue runs to four locations and roughly two dozen plans, from $29 to $599 per month, and the price of an identically named plan changes with the node. All plans are monthly, and all traffic figures are **outbound only** — inbound bandwidth is unmetered.

**Hong Kong — the flagship route**

| Plan | vCPU / RAM | NVMe | Traffic / port | Price/month | Order |
| --- | --- | --- | --- | --- | --- |
| HKG Turin Mini | 2 / 4GB | 100GB | 1TB / 2Gbps | $69 | [ Check price](https://bit.ly/Gomami) |
| HKG Turin Air | 4 / 8GB | 140GB | 2TB / 2Gbps | $129 | [ Check price](https://bit.ly/Gomami) |
| HKG Turin Pro | 6 / 16GB | 180GB | 5TB / 5Gbps | $299 | [ Check price](https://bit.ly/Gomami) |
| HKG Turin Ultra | 12 / 32GB | 220GB | 10TB / 5Gbps | $599 | [ Check price](https://bit.ly/Gomami) |
| HKG Pulse Nano | 2 / 2GB | 40GB | 500GB / 1Gbps | $49 | [ Check price](https://bit.ly/Gomami) |
| HKG Pulse Mini | 2 / 4GB | 60GB | 1TB / 1Gbps | $59 | [ Check price](https://bit.ly/Gomami) |
| HKG Pulse Air | 4 / 8GB | 80GB | 2TB / 1Gbps | $119 | [ Check price](https://bit.ly/Gomami) |
| HKG Pulse Pro | 8 / 16GB | 100GB | 5TB / 3Gbps | $269 | [ Check price](https://bit.ly/Gomami) |
| HKG Pulse Ultra | 16 / 32GB | 300GB | 10TB / 5Gbps | $499 | [ Check price](https://bit.ly/Gomami) |

**Tokyo and Singapore**

| Plan | vCPU / RAM | NVMe | Traffic / port | Price/month | Order |
| --- | --- | --- | --- | --- | --- |
| JPN Pulse Nano | 2 / 2GB | 40GB | 500GB / 1Gbps | $29 | [ Check price](https://bit.ly/Gomami) |
| JPN Pulse Mini | 2 / 4GB | 60GB | 1TB / 1.5Gbps | $49 | [ Check price](https://bit.ly/Gomami) |
| JPN Pulse Air | 4 / 8GB | 80GB | 2TB / 1Gbps | $89 | [ Check price](https://bit.ly/Gomami) |
| JPN Pulse Pro | 8 / 16GB | 100GB | 5TB / 3Gbps | $169 | [ Check price](https://bit.ly/Gomami) |
| JPN Pulse Ultra | 12 / 32GB | 300GB | 10TB / 3Gbps | $338 | [ Check price](https://bit.ly/Gomami) |
| SIN Pulse Nano | 2 / 2GB | 40GB | 500GB / 1Gbps | $29 | [ Check price](https://bit.ly/Gomami) |
| SIN Pulse Mini | 2 / 4GB | 60GB | 1TB / 1Gbps | $49 | [ Check price](https://bit.ly/Gomami) |
| SIN Pulse Air | 4 / 8GB | 80GB | 2TB / 1Gbps | $89 | [ Check price](https://bit.ly/Gomami) |
| SIN Pulse Pro | 8 / 16GB | 100GB | 5TB / 3Gbps | $169 | [ Check price](https://bit.ly/Gomami) |
| SIN Pulse Ultra | 12 / 32GB | 300GB | 10TB / 3Gbps | $338 | [ Check price](https://bit.ly/Gomami) |

**Los Angeles, the Hong Kong bulk box, and the Ryzen line**

| Plan | vCPU / RAM | NVMe | Traffic / port | Price/month | Order |
| --- | --- | --- | --- | --- | --- |
| LAX Pulse Nano | 2 / 2GB | 40GB | 1TB / 1Gbps | $29 | [ Check price](https://bit.ly/Gomami) |
| LAX Pulse Mini | 2 / 4GB | 60GB | 2TB / 1Gbps | $59 | [ Check price](https://bit.ly/Gomami) |
| LAX Pulse Air | 4 / 8GB | 80GB | 4TB / 2Gbps | $129 | [ Check price](https://bit.ly/Gomami) |
| LAX Pulse Pro | 6 / 16GB | 100GB | 8TB / 3Gbps | $259 | [ Check price](https://bit.ly/Gomami) |
| LAX Pulse Ultra | 12 / 32GB | 300GB | 15TB / 5Gbps | $599 | [ Check price](https://bit.ly/Gomami) |
| HKG Forge Mini | 56 / 128GB | 960GB | 10TB / 2Gbps | $599 | [ Check price](https://bit.ly/Gomami) |
| Ryzen 9 Mini (beta) | 2 / 4GB | 40GB | 1TB / 2Gbps | $59 | [ Check price](https://bit.ly/Gomami) |
| Ryzen 9 Air (beta) | 4 / 8GB | 60GB | 2TB / 2Gbps | $99 | [ Check price](https://bit.ly/Gomami) |
| Ryzen 9 Pro (beta) | 6 / 16GB | 80GB | 5TB / 5Gbps | $199 | [ Check price](https://bit.ly/Gomami) |

Three things worth noticing before you buy. Hong Kong carries a premium: $49 there buys 2GB of RAM and 500GB of traffic, while the same $49 in Tokyo or Singapore buys 4GB and 1TB. Los Angeles multiplies the traffic allowance — 4TB on the LAX Air against 2TB in Tokyo for the same $129 — but its Pro tier has six cores, not eight, while costing $90 more than the Tokyo Pro. And the Ryzen 9 line is flagged as beta, with the highest clock in the catalogue at 5.7GHz.

One caveat on Los Angeles: GoMami's own purchase documentation lists Hong Kong, Japan and Singapore as the available locations. LA plans appear in the store and in third-party trackers, but they aren't named in the docs, so treat that node as the newest and least documented of the four.

## Why routing is the actual product

GoMami's documentation states the latency target directly: **under 50ms RTT to mainland China**, optimised for China Telecom, China Unicom and China Mobile. It also lists Hong Kong, Japan and Singapore as its points of presence, with best-effort DDoS protection included by default and an optional 600Gbps scrubbing tier.

For a Minecraft server, this is the part that changes how the game feels. A server can have a 5GHz CPU and still be unplayable if the return path runs through congested transit. If most of your players are in China, the route is the entire reason to pay GoMami prices.

There's a catch worth stating: third-party reviews disagree about which exact route labels apply. Some report CN2 / AS9929 / CMIN2 across the Pulse and Turin lines; a Chinese-language benchmark of a Pulse box describes the same lines as China Mainland Optimized Pro on 163PP / 4837 / 58453, with CN2 GIA / 9929 / CMIN2 reserved for the Forge dedicated servers. The official docs only promise tri-carrier optimisation and sub-50ms RTT. Since a Minecraft server's players all connect through the return path, run a traceroute from a Chinese connection after the box is live — before you commit to an annual plan.

## Which plan runs Minecraft well

For most people the answer is the cheapest 4GB plan in the region nearest your players: $49/month on JPN Pulse Mini or SIN Pulse Mini, or $59 for the Hong Kong equivalent.

Here's the reasoning. World ticks, entity AI and block updates all run on the main thread, so a 2-core box serves a small server perfectly well and 2GB is where things get tight — the OS, the JVM and the world all compete for that space. Extra cores let you run more servers, not a faster one. That's why the 56-core, 128GB Forge Mini at $599 is a tool for someone running a network of worlds or reselling hosting, and complete overkill for a survival SMP.

Single-core speed is where the hardware families separate:

- **Ryzen 9 9950X (beta line)** — boost up to 5.7GHz, the highest clock in the catalogue. Best raw tick speed, with the caveat that beta product lines can carry tighter supply.
- **HKG Turin (EPYC 9575F, Zen 5)** — up to 5.0GHz, DDR5-6400, PCIe Gen5 storage. Nearly desktop-class single-core. The step from Pulse Mini to Turin Mini costs $10 and buys the newer CPU, 100GB of disk instead of 60GB, and a 2Gbps port instead of 1Gbps.
- **Pulse (EPYC 7763)** — 3.5GHz. Older silicon, same China routing, and the line that starts at $29.

For vanilla or lightly-modded play, the Pulse boxes are fine; your modpack's memory appetite will be the bottleneck long before a 3.5GHz core is. Heavy kitchen-sink packs, large-scale WorldEdit work and minigame servers where tick timing is visible are the cases where Turin or the Ryzen line earns the premium.

👉 [Compare all GoMami nodes and their current prices](https://bit.ly/Gomami)

## The real cost: annual billing and a very short refund window

GoMami's billing docs put annual billing at **15–20% cheaper than monthly**, which is where the headline price actually gets decided. Payment is prepaid, cycles run monthly, quarterly, semi-annual and annual. On the $49 JPN Mini, 15–20% is roughly $7–10 saved per month, or about $88–118 across a year.

The refund policy is 24 hours, first purchase only, and the exclusions are sharp for a game server:

- More than **10GB of traffic** within that 24-hour window voids the refund.
- An IP blackholed by a DDoS attack doesn't qualify.
- Crypto-paid orders are final, regardless of the guarantee.
- One refund per account, ever. Approved refunds delete the instance and its data immediately.

That 10GB clause is the one to plan around. Hand a fresh IP to a dozen players and bring them into newly generated chunks, and a day's traffic can clear 10GB without anyone trying. If you want a genuine evaluation, test on a new world with a whitelist.

👉 [Start with a 4GB Pulse plan at $49/month](https://bit.ly/Gomami)

## What GoMami won't do for you

The terms are unusually explicit: GoMami does not provide programming, system administration or management of individual customer systems, and it does not perform data backups for customer accounts or accept liability for data loss.

For Minecraft, that second point is the one that costs people a world. No snapshot of your region files exists on their side. Either you write a cron job that archives the world and pulls it off-box, or you accept the risk.

Billing is equally unsentimental. The service is suspended on the invoice due date with no grace period, terminated after five days overdue with data possibly unrecoverable, and invoices are generated seven days ahead so a failed card shows up in time if you're paying attention. The acceptable-use rules prohibit deliberately saturating bandwidth, CPU time or disk IO — normal server load is obviously fine, but a runaway chunk-loading loop pinning every core is your problem to diagnose.

## Setting the server up

Ordering is a five-minute job: pick node, plan and billing cycle, apply a promo code in the cart if you have one — that's the only place it accepts one — then pay by card, Stripe Alipay, crypto or account credit. Deployment completes automatically, typically within minutes.

Then the part nobody advertises:

1. SSH in, update the OS, install a current Java runtime.
2. Drop in the server jar (Paper, Fabric, NeoForge) and accept the EULA.
3. Set `-Xms` and `-Xmx`; on a 4GB box, leaving 1–1.5GB to the OS and JVM overhead is the difference between stable and swapping.
4. Open TCP 25565 for Java. If you're running Bedrock, open UDP 19132 as well, or install Geyser so one world serves both.
5. Run it under systemd or tmux so it survives a reboot, and set up your backup job the same day.

## When a managed Minecraft host is the better buy

If your players are in Europe or North America, nobody in your group benefits from China-optimised routing, and you'd rather have a panel with a one-click modpack installer than root access, GoMami is the wrong purchase at several times the price. The budget end of Minecraft hosting sits well below GoMami's $29 floor, usually on shared CPU with a management panel — which is exactly what buckles when a node is oversold, but for six friends on a vanilla world it's the rational choice.

GoMami earns its price in three situations: your players are mostly in mainland China and evening lag is the actual complaint you're trying to fix; you run modpacks or minigames where single-core clock decides whether the server is playable; or you want root access and are willing to own the maintenance.

## FAQ

**Does GoMami support Bedrock Edition?** It's a plain Linux VPS, so the official Bedrock dedicated server runs on it and listens on UDP 19132. There's no one-click Bedrock setup, and Java and Bedrock are separate server processes unless you bridge them with Geyser.

**How much RAM does a Minecraft server need?** GoMami publishes no players-per-GB guidance, and any provider that does is guessing about your modpack. Practically, 4GB is the sensible floor for a modded server, 8GB is comfortable.

**Is there a free trial?** GoMami's documentation doesn't publish one. The closest equivalent is the 24-hour refund window on a first purchase, which is void if the VM passes 10GB of traffic or gets DDoSed.

**Can I run several servers on one plan?** Yes — that's what the 8-core and 16-core tiers are for. One world won't use those cores; four will.

**What happens when I hit the traffic limit?** Traffic is outbound-only and resets each billing cycle, and GoMami sells additional traffic packs that are added to the instance's monthly quota after payment.

## Before you check out

Match the plan to the players and the world, then pay monthly for the first cycle.

- Tiny vanilla server, Asian players, tight budget → **JPN Pulse Nano, $29** (2 vCPU/2GB). Expect to tune memory settings carefully.
- Modded server or a busy survival world → **JPN or SIN Pulse Mini, $49** (2 vCPU/4GB). The default recommendation.
- Mostly Chinese players, lag is the complaint → **HKG Pulse Mini, $59**, or **Turin Mini, $69** for Zen 5 single-core and a 2Gbps port.
- Heavy modpack, minigames, several worlds → **JPN Pulse Air, $89** (4 vCPU/8GB).
- A network of servers → **Pro tier**, billed annually for the 15–20% discount.

Two checks before paying: confirm which node your players will actually route to, and set up your own backup the day the server goes live. Nothing on GoMami's side will do it for you.

👉 [View GoMami's plans and pick the node nearest your players](https://bit.ly/Gomami)
