# Accessibility Statement: CanopyWatch

I'm a Disabled civic technologist, and I build CanopyWatch with Disabled people as the primary user, not an afterthought. This page says what has been tested, what I know still needs work, and how to tell me about a barrier.

**Live tool:** https://meyeringn.github.io/canopy-watch/

## Target

CanopyWatch aims to meet the **Web Content Accessibility Guidelines (WCAG) 2.2, Level AA**.

## How it's tested

- **Automated, every week:** each live tool is scanned with axe-core against WCAG 2.1 A and AA rules. [See the latest results](https://github.com/meyeringn/meyeringn.github.io/actions/workflows/accessibility-check.yml).
- **Reduced motion:** the tool respects your device's "reduce motion" setting.
- **Manual review:** not yet completed. Planned: keyboard-only use, NVDA and VoiceOver screen readers, and 200% zoom on a phone-width screen.

Automated tools catch only some barriers. Until the manual review is done, please treat this tool as tested by machine, not yet by people.

## Fixed in November 2026

The first automated scan found issues that are now fixed: low-contrast text on tabs, notes, badges, and action chips; map grid roles; tab labels; and footer link styling.

## Known issues

| Issue | Who it affects | Workaround | Status |
| --- | --- | --- | --- |
| Neighborhood names inside the map grid are printed very small. | Low vision users | Each square has a full spoken label, and selecting it opens the detail panel in larger text. Browser zoom also works. | Planned |
| Hover tooltips only appear with a mouse. | Keyboard and touch users | The same facts appear in each square's label and in the detail panel. | By design |
| Automated checks cover the opening Neighborhood Map tab; the other four tabs have not yet been checked separately. | Everyone | Report anything you notice. | Planned |

## Report a barrier

If something in CanopyWatch doesn't work for you, I want to know.

- [Open an issue](https://github.com/meyeringn/canopy-watch/issues/new?title=Accessibility%20barrier) (requires a free GitHub account), or
- Email meyeringn@gmail.com with "Accessibility" in the subject line.

Please describe what you were trying to do, what happened, and what device, browser, or assistive technology you use. I aim to reply within 5 business days.

**Last updated:** November 2026
