1. Make the plugin file executable
   chmod +x /workspaces/AsciiArtify/scripts/kubeplugin
   
2. Copy file to folder in $PATH with name kubectl-kubeplugin, or make a symlink, e.g.:
   sudo ln -s /workspaces/AsciiArtify/scripts/kubeplugin /usr/local/bin/kubectl-kubeplugin

**Usage**
The information about node resource:
kubectl kubeplugin node

The information about pod resource in the specified namespace, assumed default if not specified:
kubectl kubeplugin pod kube-system
