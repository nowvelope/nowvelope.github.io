# Agent instructions for the Nowvelope website

## The privacy policy

`privacy.html` is Nowvelope's public privacy policy. The app repository's
`PRIVACY.md` is the detailed engineering record of how the app behaves; this
page is not a copy of it.

### Say what data is involved and why, not how the app does it

The policy tells people what data the app uses, keeps and shares, why, and
what they control. It does not describe the implementation. If an internal
change, such as a new algorithm, a different framework, a timeout or a renamed
screen, would make the page wrong, the page is too specific.

- ✅ "uses the compass to record which way the panorama faces and to keep the
  capture lined up"
- ❌ "reads the compass through Core Motion's true-north frame and pairs it
  with each accepted photo"
- ✅ "only if you choose to include it"
- ❌ "unless you turn on Include Location in Settings"
- ✅ "the measurements made while capturing, which can reveal a room's layout"
- ❌ "ARKit's world map, LiDAR depth and a 3-D mesh"

Name a data category and its purpose ("location, to name the panorama"), name
who receives anything that leaves the device ("Apple's map service"), and name
what the user controls ("off until you turn it on"). Leave out frameworks,
setting names and menu paths, request formats, durations, and how many times
something is sampled.

### Don't overpromise

Every sentence is a commitment. Before keeping or adding a claim, check that it
holds for every iPhone the app supports and every setting the user can choose,
and that it will stay true without deliberate effort. Prefer "may" or "can"
where the app's behaviour depends on the phone or the user's choices. A
sentence that names something the app never does ("never your picture", "no
background recording") must be checked against the code, not the old page.

### When the page needs to change

Update it when what the app uses, keeps or shares changes: a new kind of data,
a new purpose for existing data, anything newly leaving the device, a new
permission, or a change to what the user controls. Do not update it for a
change in how the app does what it already describes. A new use of data the app
already collects is a new purpose, so check whether the page's stated purposes
still cover it; if they do, no change is needed.

When it does change, bump "Last updated" at the top of the page, and say in the
pull request which app change prompted it.
