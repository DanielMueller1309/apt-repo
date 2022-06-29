# ansible-role-apt-repo

Add apt keys and apt repositories.

## Debian and PPA

The role, deliverately, does not support adding PPA repositories in Debian.

# Requirements

None

# Role Variables
```yml
apt_repo:
  - repo_name: brave
    repo_link: "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"
    repo_key: "https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg"
    repo_keyring: "/usr/share/keyrings/brave-browser-archive-keyring.gpg"
apt_repo_enable_apt_transport_https: true
```

# Dependencies

None

# Example Playbook

```yaml
- hosts: localhost
  roles:
    - DanielMueller1309.apt-repo
  vars:
    apt_repo:
      - repo_name: brave
        repo_link: "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"
        repo_key: "https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg"
        repo_keyring: "/usr/share/keyrings/brave-browser-archive-keyring.gpg"
    apt_repo_enable_apt_transport_https: true
```

# License

```
Copyright (c) 2016 Tomoyuki Sakurai <tomoyukis@reallyenglish.com>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

# Author Information

Tomoyuki Sakurai <tomoyukis@reallyenglish.com>
