==TEMPO reliability==
- [x] james debugging crashes
	- [x]  create tcm, geofence service, drag ttp?
	- [x] no real specific set of actions to reproduce yet
- [x] do a clean build, verify tiles, stress test, see if more 
	- [x] maybe do a release build? to avoid assert crashes?
- [x] widows never seem to popup in running instance of C2, always have to restart C2

==TEMPO UX==
- [ ] TCM saving/loading for one time digitization persistence
- [ ] routes with chevrons or some directional indicator
- [ ] TCM association tag should allow TCM creation
- [ ] controls context-sensitive menu that tells user what they can do
	- a la hypergiant

==Map tiles==
- [ ] in addition to verifying JJs tiles, upload QGC tiles, get that working

==Feedback collection==
- [ ] auto screen record w/ tempo alias

---
## 3/24 Notes

- don't allow ttp execution w/ invalid params, just gray out execute button or enforce range
- geofence service needs to be easier, but also just officially redone
- maybe if no TCM for TTP, we prompt user to draw TCM
	- just be able to create TCM from association indicator
- c2hitl popups need to be aware of observing multiple targets with one drone
- [x] ==route shouldn't be white==
- route should indicate direction (for muster)
- RTL workflow needs work, maybe a button on agent panel for each one
	- selection is annoying
- selecting agents is clunky (deselection specifically)
	- deselection should auto occur after sending a TTP or create a clear agents button
- RTL ICON WAS RED???
	- not able to replicate in sim
- tactic chaining process is unintuitive and a little small
- add more identities to situation objects and orientation
- debugger good, make its usage better
- [x] ==copy tiles from original build to hot fixed build==
- [x] ==get JJ to get more tiles==
- [ ] ==create checklist for soldiers==
- perimeter scan never completes :)
- clearing situation objects
	- clear button doesn't sound right
	- time aspect sounds right, but how
- set battery failsafe from UI

---
## 3/25 Notes

### Observations:
- we lost comms about 1.5km out from radio and single drone
- improved comms to about 2km using a repeater drone
- drones tasked with Observe appear a different color
	- could be linked to drones that lose comms and then come back
	- nothing bad happened though (pog)
### Todos:
- test QGC app image on tablet, tomorrow
- test ATR around the TAA and get a ratio of false positives to real ones
- get unified operator view feedback from Cpt. Max Laguna
- make geofence service auto push to drones
### Needs:
- support QGC tiles
- support TAK interface for TCM ingestion
- allow for MGRS input
- permanent dismissal of situation objects
	- drone is stationary and repeatedly detecting the same false positive
- get thermal cameras going w/ ATR
- training our ATR model using the imagery the operator receives and the identification they input
- bring a footage mule drone
### Matt Notes
- TCM export/import
- better ATR and training on their vehicles, take footage
- operator confirm a detection before publishing to TAK
	- Cpt. Laguna has experienced a diff system just flooding TAK
- interest in mesh network, to reach farther distances and maintaining comms, get more out of the cheaper platforms
- making a user story to represent their workflow
	- pulled up a phone w/ a picture of a physical map that had MGRS coordinates with marker on it
	- also on TAK stuff, we want to automate things
- allow users to import custom maps (or map layers, etc.)
	- allow users to use maps they are used to

---
## 3/26 Notes

### Observations:
- our comms stopped working
	- probably sync's fault (James saw similar thing)
- ImGui status bar still receiving click behind windows (maybe just disable this honestly)
	- settings menu is needed, but we need window layout
- radial fence issues and sometimes pushing to drones not working when they were restarted
- RTL always completes as red
- lost comms, QGC return didn't work
	- return resulted in land in place
- TCM sync issues when restarting
- tactic chaining with selected agents feels weird w/ the tactic agent count parameter field
	- default value should probably be based on parent tactic's agent count
	- default value needs to be dynamic based on context
### Todos:

### Needs:
- land tactic to not give away position
	- they typically pop in/out of concealment to hand launch
	- accommodate this
- some operators don't have all coordinates, really need ATAK TCM ingestion
- improved image clarity and size
	- allow zooming within image itself

### Matt Notes:
- QGC land in place
- restart C2 to regain connection to RTL
- system comms stopped working even with good network
- on restarts, task status was gone in agent visuals as they were executing
	- shouldn't have to restart the UI
	- if we do, it shouldn't break