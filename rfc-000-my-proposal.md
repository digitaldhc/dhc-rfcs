# My RFC Title

## Summary

A proposal to introduce a standard for creating published service URL names.

## Problem

Currently service URLs are constructed using the DNS A record for the server – this being in most cases the server name. This means that either the URL has to change when the system is migrated to another server, or the new server has to have the same name as the old server. These names are cumbersome to both say and type, e.g. seinfboprod01.dhc.nhs.uk.

## Proposal

I am proposing the formal adoption of a dedicated subdomain in our DNS infrastructure called **service.dhc.nhs.uk**, to be used solely for the clear and unambiguous naming of published services using CNAME aliases to point to the correct A record. This subdomain is already in existence and has been used informally for some years however this has not been universal. 

The use of a subdomain for published services such as this potentially has a number of benefits:
	
- the use of CNAMEs means that as long as the system is live the URL used to access it does not need to change;
- the service subdomain provides a clear and unambiguous indication that this is a service published and provided by Dorset HealthCare;
-	it meets the example set by central government in their use of a dedicated service.gov.uk subdomain for published services;
-	it masks overly complex URLs, particularly those that may exist on internet hosted services where ownership of the service is not clear – e.g. https://dhunft.outsystemsenterprise.com/FOI_Web/ could become https://foirequest.service.dhc.nhs.uk/FOI_Web/.

Internet-facing subdomains and CNAMES are supported by the NHS Digital networking addressing namespace policy.

I would further propose that we consider how we name published services as there has been some confusion about this in the past. The government service naming guidelines propose the following (paraphrased):
	
- use words and terminology that people use;
-	describe a task, not a technology;
-	choose a name that doesn’t need to change when policy or technology changes;
-	use verbs, not nouns;
-	don’t use department or agency names;
-	don’t use names that are brand-driven.

Not all of these factors will be appropriate for our use but are I suggest worthy of consideration.

An extra consideration might be whether we need to think about a defined “start page” on Doris or the Trust’s public website for services, either individually or in groups. A start page would include the following:
	
- the name of the service;
-	a short introduction to the service to help people understand what it does;
-	a “start now” button to access the service;
-	a list of other ways to access the service;
-	where to find support for a service.

Start pages would not be necessary or appropriate for all systems but may add value to others.
