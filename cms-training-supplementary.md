
# Creating a group (slide 48)
## If you did not, or were for some reason unable, to create a group through the portal
```
 slate group create cms-training-<your initials> --field "High Energy Physics"
```

# Getting Command Line Access (slide 60)
## (Optional - this is preinstalled on the training system)
Download the SLATE client for Linux:
```
curl -LO https://jenkins.slateci.io/artifacts/client/slate-linux.tar.gz
```
Download and check the checksum:
```
curl -LO https://jenkins.slateci.io/artifacts/client/slate-linux.sha256
sha256sum -c slate-linux.sha256
```
Unpack the client:
```
tar xzvf slate-linux.tar.gz
```
Set your search path to find the client:
```
export PATH="$PATH:$(pwd)"
```

# Registering a cluster (slide 68)
Use the slate cluster create command to register your cluster:
```
slate cluster create cms-cluster-<your initials> --group cms-training-<your initials> --org "U.S. CMS"
```
Agree to all prompts.


# View cluster information (slide 69)
View your cluser's information with:
```
slate cluster info <your cluster name>
```

Check that the federation is able to reach your cluster with:
```
slate cluster ping <your cluster name>
```
