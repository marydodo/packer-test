# Packer Intro. Installing Packer.

[/] Install packer binary

[/] Verify the Installation

[/] Build an Image

---  [/] Create Template
 * Used example template from Learn Docs
 * named it _example.pkr.hcl_

---  [/] Verify Template

---  [/] Build First Image with AWS EC2 AMI

  * Using the packer build command, my first image with AWS EC2 was born.

---  [] Learn How to Manage Image

[] Provision

---  [] Configure Provisioners

---  [] Launch AMI

[] Investigate Parallel Builds

[] Investigate Vagrant Boxes

---  [] Enable Post-Processor

---  [] Learn how to use Post-Processor

## Questions, comments, concerns, etc.

### What is a machine image?

A machine image stores all the configuration you want to help create a virtual machine (VM) instance.

### Why use machine images?

With machine images, you can take a snapshot of your web application and save it to a unique machine image. You can then use that machine image to launch multiple instances that are configured in the exact same way as your source instance.

### What is Packer?

Packer is a Hashicrop IaC tool that makes automating machine image creation easy. Encourages automation of **scripts** to _install_ and _configure software_ within Packer-made images with unique machine image IDs.

## Issues

1. During the "Verify Template" stage, I ran into an issue with the example template from Learn Docs. The issue was with two specific lines. These lines have been commented out of the _example.pkr.hcl_ template file. After removing these lines, packer was able to verify the template.

```
  access_key    = "${var.aws_access_key}"
  secret_key    = "${var.aws_secret_key}"
```
