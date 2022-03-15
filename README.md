# BYONI

Because we can always use more acronyms, BYONI stands for **B**ring **Y**our **O**wn **N**otebook **I**mage.

## What this is

Red Hat OpenShift Data Science comes with a curated list of Notebook Images.

* Some of them come by default with RHODS
* Others are provided by ISVs

You can also bring your own ("BYO") notebook images and add them to the list of available images. Check the [Official Documentation](https://access.redhat.com/documentation/en-us/red_hat_openshift_data_science/1/html/managing_users_and_user_resources/managing_notebook_servers#configuring-a-custom-notebook-image_user-mgmt) for more info.

This particular repo is a list of image definitions that we tend to use often.

## Support

No support is provided.

## Requirements

For now, you have to be cluster-admin to be able to add and image.

## Caution

Because you are working in the same Namespace as RHODS (`redhat-ods-application`), care should be taken to not damage any of the other images.

## Instructions

### Clone the project

```bash
git clone https://github.com/rh-aiservices-bu/byoni.git
cd ./byoni
```

### Pytorch with Audio

```bash
oc -n redhat-ods-applications apply -f ./images/pytorch-with-audio/pytorch-with-audio.yaml
```

### Elyra

```bash
oc -n redhat-ods-applications apply -f ./images/elyra/elyra.yaml
```

### R

```bash
oc -n redhat-ods-applications apply -f ./images/r/r.yaml
```

