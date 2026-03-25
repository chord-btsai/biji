==TEMPO reliability==
- [x] james debugging crashes
	-  create tcm, geofence service, drag ttp?
	- no real specific set of actions to reproduce yet
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
- ==route shouldn't be white==
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
- ==copy tiles from original build to hot fixed build==
- ==get JJ to get more tiles==
- ==create checklist for soldiers==
- perimeter scan never completes :)
- clearing situation objects
	- clear button doesn't sound right
	- time aspect sounds right, but how
- set battery failsafe from UI
- 