---
layout: post
title: "First post in Jekyll"
categories: "example"
---

GCP has a hierarchy of Organisation, Folder, Project.

Organization is the top level, followed by the folder, and the project.

Organization —> Folder —> Project

**Project**

The Project is the baseline of Google cloud platform.  We provision the resources, setup infrastructure in the project. 


![Gcp project](/assets/gcp-project.png)



**Folder**

Folder is used to group and manage the projects under the organisation. Similar to operating system folders, in GCP, a folder can contains projects and sub-folders as well.

We can't provision any resources in the folder. It is strictly for managing projects in terms of IAM permissions and billing.

Permissions granted at Folder level are inherited by sub-folders, projects. 

Note: A Project needn't to be a part of folder. It can directly created under an organisation.

![Gcp folder](/assets/gcp-folder.png)



**Organization**

Organization is top-level unit of GCP hierarchy. 

An Organization resource is automatically created when user associated with a G Suite domain creates a project or billing account. Also Organization is associated with exactly one domain, which is set when the Organization resource is created.

Say if you have a gsuite domain called [example.com](http://example.com), then your GCP organization will be set as example.com and your folders, projects will be created under this organization.

Permissions set at the org level, trickle down to folders and projects. So it is not a recommended practice to provide access at an org level, unless someone needs access to all the projects.


![Gcp Organization](/assets/gcp-org.png)


**Summary**

In this quickstart, You have seen what is a project, folder, organization in Google Cloud Platform. 
In the upcoming posts, I'll write 101s of IAM, Storage, Compute, Network, etc.,

If you like this post, please share and comment.

