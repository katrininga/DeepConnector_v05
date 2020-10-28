# DeepConnector_v05

A tool for Nuke. Deep Merge that collects all DeepReads in script, creates check box knobs from the filenames to select and connects to.
This tool is mainly designed for scripts that include a lot of Deep nodes, especially to create holdouts. 


The DeepCollector is a customized "Deep Merge". Within the "Deep Merge" are custom buttons. "Refresh", "Collect to:", "Connect" and check box knobs with names of all "DeepRead" files in the script.

The "Refresh" button creates checkbox knobs(Boolean knobs) from file names from DeepRead nodes in the script. 
If there are two or more DeepReads with the same file, the check knob will become red and show in brackets at the back how many copies exist in the script.
If there is a new DeepRead in the script, the knob for it will appear green.
Then you can select which Deepread you want to connect to by checking the checkbox knob next to its filename.

"Connect to:" allows you to choose if you want the merge to connect to the DeepRead it self or the DeepReformat connected to it.

"Connect" connects the DeepMerge node to all Deepreads or Deepreformats that have maching filenames to the check knobs that have been selected/checked.
If the "Connect to:" is set to "Reformat" it will Connect to the DeepReformat nodes underneath the Deepread.
If a DeepRead is not connected to a DeepReformat, an Error message will pop up that tells you which DeepReads aren't connected to a DeepReformat and not connect to those.
If "Connect to:" is set to "Read" it will connect directly to the DeepReads.
When there are two or more of DeepReads that hold the same file, the DeepConnector will only connect to one of them. If only one has "DeepReformat" attached and the "Connect to:" is set to "Reformat", it will pick that DeepRead over the others.





