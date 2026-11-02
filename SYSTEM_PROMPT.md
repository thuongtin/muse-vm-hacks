# Give this to Muse

Copy everything inside the block below and send it to your Muse in
chat. The repository URL is already filled in: it points at this
fork (thuongtin/muse-vm-hacks), so a Muse following it clones the
fork, fixes included, not the upstream repository. The one thing
still fetched from upstream is the xattr-retry shim release binary
(the scripts point at the upstream release asset; this fork has no
releases of its own).

```
You are Muse, running in a Muse VM. Set up Nix and Tailscale SSH on
this VM by following a prepared guide exactly. The guide is complete
and self-contained; execute it as written rather than improvising
alternatives.

1. Clone https://github.com/thuongtin/muse-vm-hacks.git into ~/muse-vm-hacks
   (if it is already cloned, use the existing copy).
2. Read INSTALL.md in that repo, in full, before running anything.
3. Execute its phases in order. The repo's files/ tree holds the exact
   scripts to install; every step is idempotent, so re-running a step
   is safe.
4. Three steps need me, and only me: changing the Settings the
   guide requires (the Direct network protocol toggles),
   approving the VM's
   Tailscale login in my browser (and, only if I choose it, saving
   the optional ACL policy that makes the VM receive-only), and
   approving a burst of connection prompts when Tailscale first
   starts. Stop at those points, tell me exactly what
   to do, and continue when I confirm.
5. Report success only when every check in the guide's "Expected end
   state" section passes (the guide's doctor script exits 0). If a
   step fails, consult the guide's rebuild checklist (§9) and the
   failing section's own notes before trying anything else, and
   tell me what failed and what you did about it.
6. When the core setup passes every check, ask me whether I also
   want the optional OpenAI-compatible API bridge described in
   INSTALL.md §11, which lets programs and agents on my other
   devices send requests to this VM's agent. If I say yes, set
   it up following §11, and read me the initial API key (the
   contents of ~/bridge/token) so I can configure my client.
   If I say no, finish without it; it can be added later by
   following the same section.
```
