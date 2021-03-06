---
layout: post
title: "Recipe: Programmatically Creating and Updating AWS security groups"
date: 2011-12-19
comments: false
---

<div class='post'>
    I think I've rewritten this code 3 times now in the last year so it seems prudent to save it somewhere. &nbsp;If
    other folks find it useful that'd be great.<br /><br />The problem is a simple one. &nbsp;You're looking to setup
    and install of a few machines on EC2, perhaps to run something fun like a Cassandra cluster.<br /><br />Typically
    it's really tempting to just setup the security group once and never ever touch it again. &nbsp;I'd log into the the
    AWS console, and following along with&nbsp;<a href="http://www.datastax.com/docs/1.0/install/install_ami">this
        datastax guide</a>&nbsp;I would manually setup the group, launch instances, etc.<br /><br />However, without
    automation there's some duplication of effort whenever someone on your team sets up a cluster and possibility for
    user error setting up security groups. &nbsp;And of course we're already automating the other important bits like
    "launch a new instance" or "run a backup" already so why not manage security groups with the same
    scripts?<br /><br />I'm currently working with&nbsp;<a href="http://docs.fabfile.org/">Fabric</a>&nbsp;to automate
    EC2 stuff so I pulled out the Python code I'm using to handle creation of security groups and permission rules
    within those groups.<br /><br />The script attempts to be idempotent. &nbsp;The idea here is that simply rerunning
    the script will, only if necessary, create groups, revoke old rules and authorize any new ones. <br /><br />Anyway,
    without further ado <a href="https://gist.github.com/1498451">here's the script</a>:
    <script src="https://gist.github.com/1498451.js?file=aws_sg_recipe.py"></script><br /><br /><br /></div>