---
format: 
 html:
  theme: light
  css: assets/css/styles.css

title-prefix: Bloomington Mesh
pagetitle: Welcome

---
::: {style="text-align: center; color: #990000;"}
# Bloomington Mesh
_Locals meshing together in Bloomington, IN._
<hr>
:::
# Welcome!

If you live near Bloomington Indiana and want to join a local mesh network, we would love to have you!
We mostly run [Meshcore](https://meshcore.io/) firmware, but a couple of us still run [Meshtastic](https://meshtastic.org/) either alongside or instead.


# Join the Community

We have primarily organized on Signal, a secure and privacy-respecting messaging app. Join our <button id="signal-modal-trigger" class="signal-modal-trigger" type="button">Signal group</button>. Additionally, you can find us on the [Indiana Mesh Discord](https://discord.gg/RAnPvDsxPJ).

<div id="signal-modal" class="signal-modal" aria-hidden="true" role="dialog" aria-modal="true" aria-labelledby="signal-modal-title"><div class="signal-modal-dialog"><button id="signal-modal-close" class="signal-modal-close" type="button" aria-label="Close">×</button><h2 id="signal-modal-title">Complete the challenge to join</h2><p>We use an anti-bot check before revealing the Signal invite link.</p><div id="signal-turnstile" class="signal-turnstile"></div><a id="signal-link" class="signal-link" href="#" aria-disabled="true" tabindex="-1">Join the Bloomington Mesh Signal group</a></div></div>

<script src="https://challenges.cloudflare.com/turnstile/v0/api.js?onload=turnstileOnLoad" async defer></script>
<script>
  (function () {
    const trigger = document.getElementById("signal-modal-trigger");
    const modal = document.getElementById("signal-modal");
    const closeButton = document.getElementById("signal-modal-close");
    const signalLink = document.getElementById("signal-link");
    const siteKey = "0x4AAAAAAGBR6mXm29ZVZeW1";
    const encodedSignalLink = "aHR0cHM6Ly9zaWduYWwuZ3JvdXAvI0NqUUtJTnl5b2x4TEVQUWpOLUdWRTVTVTAwdVNUQXpDMVpQNTFxR1kxay1sWUk5dUVoQnN3RHJ6VXExVlJGd0ZEVEQtdHFyZw==";
    const decodedSignalLink = window.atob(encodedSignalLink);
    let turnstileWidgetId = null;

    function disableSignalLink() {
      signalLink.href = "#";
      signalLink.setAttribute("aria-disabled", "true");
      signalLink.setAttribute("tabindex", "-1");
      signalLink.classList.remove("is-enabled");
      signalLink.removeAttribute("target");
      signalLink.removeAttribute("rel");
    }

    function enableSignalLink() {
      signalLink.href = decodedSignalLink;
      signalLink.removeAttribute("aria-disabled");
      signalLink.removeAttribute("tabindex");
      signalLink.classList.add("is-enabled");
      signalLink.setAttribute("target", "_blank");
      signalLink.setAttribute("rel", "noopener noreferrer");
    }

    function renderTurnstile() {
      if (!window.turnstile || turnstileWidgetId !== null) {
        return;
      }

      turnstileWidgetId = window.turnstile.render("#signal-turnstile", {
        sitekey: siteKey,
        callback: function () {
          enableSignalLink();
        },
        "error-callback": function () {
          disableSignalLink();
        }
      });
    }

    function openModal() {
      modal.classList.add("is-open");
      modal.setAttribute("aria-hidden", "false");
      disableSignalLink();
      if (window.turnstile) {
        renderTurnstile();
      }
    }

    function closeModal() {
      modal.classList.remove("is-open");
      modal.setAttribute("aria-hidden", "true");
      if (window.turnstile && turnstileWidgetId !== null) {
        window.turnstile.reset(turnstileWidgetId);
      }
      disableSignalLink();
    }

    trigger.addEventListener("click", openModal);
    closeButton.addEventListener("click", closeModal);
    modal.addEventListener("click", function (event) {
      if (event.target === modal) {
        closeModal();
      }
    });
    document.addEventListener("keydown", function (event) {
      if (event.key === "Escape" && modal.classList.contains("is-open")) {
        closeModal();
      }
    });

    disableSignalLink();
    window.turnstileOnLoad = function () {
      renderTurnstile();
    };
  })();
</script>

**To cut down on spam, we ask that you introduce yourself within 24 hours of joining**. A simple "Hi, I'm _[name]_, I work in _[industry/profession]_, and I'm interested in mesh networking!" is sufficient. 

If we don't hear from you, you will be removed from the group. When joining, please use a name we can recognize, though it doesn't have to be your full name. _(Please don't use `.exd`, for example!)_ We look forward to meeting you!

# What is Meshcore?

Meshcore is an open source, off-grid, decentralized, mesh network built to run on affordable, low-power devices. You can join and be off to a great start with $50 or less. To learn more, [check out our friends at OKIMesh.org](https://okimesh.org/)!

You will need the following to get off to a good start:

- A compatible 915MHz LoRa device
- Proper antenna for your device (the stock antennas that come with the devices are often not ideal, so consider upgrading to a better antenna for improved range and performance)
- A smartphone or computer with a USB A port and a Chrome-based browser to configure the device and communicate with other users

An alternative but similar mesh networking project is [Meshtastic](https://meshtastic.org/) which runs on some of the same radios. Meshtastic and MeshCore do not exchange messages directly over the air. If you are choosing firmware, use what the people you want to reach are running. While the area primarily uses Meshcore, Meshtastic users are also welcome. All meshers are welcome!

# Help Wanted

Our community is just getting started, and everyone is welcome to contribute!

Currently, the downtown and campus area has pretty good coverage with Meshcore nodes, but the surrounding area is lacking coverage. We welcome anyone who wants to help expand the network. **We especially need places to put repeaters. If you own a site that could host one, please let us know!**

## Site

This site was originally written by [kratcliff](https://github.com/kratcliff) and was rewritten using Quarto by [lucasburlingham](https://github.com/lucasburlingham). The source is avaliable at [kratcliff/btownmesh.org](https://github.com/kratcliff/btownmesh.org), and is hosted using GitHub Pages. See an issue or a revision to be made? Make a pull request!
