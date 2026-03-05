# 🪟 Disable Windows 11 Updates — Registry Files

Resources for the video: **"Top 5 Ways to Disable Windows 11 Updates (From Easy to Advanced)"**  
📺 [Watch on YouTube](https://www.youtube.com/LINK_HERE)

---

## Files

### `disable-windows-updates.reg`
Applies the following Registry policy:
```
HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU
  NoAutoUpdate = 1
  AUOptions    = 2
```
**Effect:** Windows stops downloading and installing updates automatically.  
**Works on:** Windows 11 Home, Pro, Enterprise (all editions).

---

### `reenable-windows-updates.reg`
Removes the keys above entirely.  
**Effect:** Windows Update returns to default behavior.

---

## Which Method Is This?

This is **Method 4** from the video — the Registry approach.  
It's the equivalent of Group Policy Editor settings, but works on **Windows 11 Home** too.

For the other 4 methods (Metered Connection, Services, Group Policy, Firewall), see the full video.

---

## Troubleshooting

**"Windows Update still runs after applying the .reg file"**  
→ Make sure you restarted your PC after applying  
→ Check if Windows Update Medic Service is re-enabling it — use Method 2 (services.msc) alongside this

**"I can't run the .reg file"**  
→ Right-click → Run as administrator

**"I want to undo this"**  
→ Double-click `reenable-windows-updates.reg` and restart
