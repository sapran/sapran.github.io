---
id: 894
title: My article in Hakin9 magazine Issue 7/12
date: 2012-08-28T20:13:00+00:00
author: sapran
layout: post
guid: http://styran.com/2012/08/28/my-article-in-hakin9-magazine-issue-712/
permalink: /2012/08/my-article-in-hakin9-magazine-issue-712/
blogger_blog:
  - securegalaxy.blogspot.com
blogger_author:
  - Vlad Styran
blogger_permalink:
  - /2012/08/my-article-in-hakin9-magazine-issue-712.html
blogger_internal:
  - /feeds/3388835630659782197/posts/default/3510648258831171962
shorturl:
  - http://tinyurl.com/pzcesyf
categories:
  - Uncategorized
tags:
  - Uncategorized
---
<div dir="ltr" style="text-align: left;">
  I wrote an article on some basic intel & recon related to Social Engineering audits. You can find it in the latest <a href="http://hakin9.org/samuraiwtf-toolkit-exploiting-software-0712/?a_aid=nataliaboniewicz&a_bid=8f6377e8"><b><i>Hakin9 issue</i></b></a>&nbsp;where it&nbsp;original&nbsp;appeared, or just continue reading.</p> 
  
  <div style="clear: both; text-align: center;">
    <a href="http://hakin9.org/samuraiwtf-toolkit-exploiting-software-0712/?a_aid=nataliaboniewicz&a_bid=8f6377e8"><img border="0" height="200" src="http://1.bp.blogspot.com/-q7SgcKLP_4I/UD0m2xp_RxI/AAAAAAAATtk/z4M4P_iUyMI/s200/01.jpg" width="138" /></a>
  </div>
  
  <div style="text-align: center;">
    <b>Picking Up Mushrooms in the Rain Forest</b>
  </div>
  
  <div style="text-align: center;">
    <b>Social Engineering Information Gathering</b><br /><b><br /></b>
  </div>
  
  <div>
    Social Engineering is a field of information security industry that is both known and unknown to general public. On the one hand, there is a number of world known social engineers, from both the dark and the bright side of the trade, whose adventures are captured in numerous movies and&nbsp;memoirs&nbsp; While on the other hand social engineering is one of the topics that are full of speculation and uneducated claims, including those in the media, and that sadly turns social engineering into some kind of a gray area.<o:p></o:p>
  </div>
  
  <div>
    <a name='more'></a>
  </div>
  
  <div>
    In the meanwhile, social engineering infiltrates a substantial part of computer security operations. To name few, Security Awareness, despite its arguable efficiency, is the set of information security controls directed to decrease the probability and potential impact of security incidents caused by inherited vulnerabilities of human nature. Also, social engineering vector, or as we often call it Social Channel, is an integral part of a robust penetration test according to every modern methodology in this field. Not to mention the variety of human factor threats facilitated by the ubiquity of the Internet, such as phishing, 419 scam, email and social networks spam and so on and so forth.</p>
  </div>
  
  <div>
    Obviously enough, knowing all this does not make any one of us a (Anti) Social Engineering expert. For several decades now we (and by ‘we’ I mean information security professionals) have known that ‘human factor’ is the cause of something around 80% security threats and did almost nothing to deal with that. While network channel of attack keeps increasing the difficulty of its exploitability, social engineering tricks work as they used to for Kevin Mitnick and Frank Abagnale. And sometimes even better (or worse, depending on your perspective) because there are many times more people targets accessible by the attackers nowadays.</p>
  </div>
  
  <div>
    So, what can we do? Many things, in fact. First of all, if Social Engineering threats constitute a significant threat to your business, revise your business model. Can you remove people component from it? I guess, no. Then, you have to change or educate people and that is the hard part.<o:p></o:p>
  </div>
  
  <div>
    As I said, people are inherently vulnerable because… they are people. People are willing to talk, trust, and share to each other and that is both to our benefit as a species and disadvantage as individuals. It may seem funny, but all the things that helped us develop the society can be used in malicious purpose by immoral individuals.</p>
  </div>
  
  <div>
    The complete course of action that may increase your resistance to Social Engineering attacks would take a book to briefly describe and I am going to recommend some of existing books in the end of this article. As a quick start I recommend to conduct an audit and learn from it. For some using audit techniques in the beginning of information security program may seem unnatural, but think about it: can we start any improvement without sufficient knowledge of our current state? I strongly doubt it. In this article we’ll discuss some aspects of social engineering penetration testing, in particular information gathering. There is a very small chance of successfully assessing security when it works. Instead, usually it takes a hard time of trying to break it. And there unlikely is a field in pentesting that is more sensitive to proper information gathering than social engineering audit.</p>
  </div>
  
  <div>
    So, let’s start with a threat model. Roughly speaking, there is a target or ‘mark’ that is our goal in a pentest. Most of the time it’s all about getting sensitive information important enough to be further leveraged in order to get and maintain access to IT systems, or alternatively be used directly in order to demonstrate risk to the client’s business. The mark can be also an action by individual (e.g. personnel) that can facilitate the attack: influencing guards to grant access us to restricted area, or making a person click malicious link or open uber-APT-dropping email attachment can be another goal. Keeping all the SE methods and techniques out for the time being, there is one thing lack of which renders all that SE ‘dark art’ useless: Information. Gathering sufficient amount of information is vital in a pentest, and the type of information we are looking for strongly depends on what result we want to achieve.</p>
  </div>
  
  <p>
    <span style="line-height: 115%;"><span style="font-family: inherit;">In the course of this article, let’s assume that our goal is to contact some of the client’s employees and present them with email with our ‘special’ attachment, or a link to some crafted or cloned web-site. While the former is often used in order to gain access to the client’s network, the latter is a tool of choice for credentials harvesting. So, it seems like we need some email addresses, right? First thing that comes to mind is, of course, using a search engine such as Google. Unfortunately almost all of them are doing a good job of keeping this type of data not that easy to find. Try to search for some sort of email yourself and you will see that the regular approach works pretty well when you are searching for a specific email, but fails miserably once you try to find some new, unknown emails in a specific domain. So, what can we do to search for <a href="mailto:usernames@client.com">usernames@client.com</a>?&nbsp;</span></span><br /><span style="line-height: 115%;"><span style="font-family: inherit;"><br /></span></span> 
    
    <div>
    </div>
    
    <div>
      Sure thing, there are some tools for that. First, look at theHarvester, an easy to use information gathering tool. Fire up your BackTrack and find it in <span style="font-family: &quot;Courier New&quot;; font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">/pentest/enumeration/theharvester/theHarvester.py</span>. The tool takes many options, the most important of which are <b>what</b> to search for and <b>where</b>: -d and -b options respectively.&nbsp;<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">noroot@bt:/pentest/enumeration/theharvester$ ./theHarvester.py <o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">Usage: theharvester options <o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -d: Domain to search or company name<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -b: Data source (google,bing,bingapi,pgp,linkedin,google-profiles,people123,jigsaw,all)<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;-s: Start in result number X (default 0)<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -v: Verify host name via dns resolution and search for virtual hosts<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -f: Save the results into an HTML and XML file<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -n: Perform a DNS reverse query on all ranges discovered<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -c: Perform a DNS brute force for the domain name<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -t: Perform a DNS TLD expansion discovery<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -e: Use this DNS server<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -l: Limit the number of results to work with(bing goes from 50 to 50 results,<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; -h: use SHODAN database to query discovered hosts<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; google 100 to 100, and pgp doesn&#8217;t use this option)<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">Examples:./theharvester.py -d microsoft.com -l 500 -b google<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ./theharvester.py -d microsoft.com -b pgp<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ./theharvester.py -d microsoft -l 200 -b linkedin<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">noroot@bt:/pentest/enumeration/theharvester$<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;"><br /></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div>
      Let’s type some demo commands to show its power. In line with some other information, the command <span style="font-family: &quot;Courier New&quot;; font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">./theHarvester.py -b all -d hakin9.org</span> will also show this section:<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">[+] Emails found:<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">grzegorz.tabaka@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">andrzej.kuca@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">ireneusz.pogroszewski@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">ewa.dudzic@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">patrycja.przybylowicz@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">karolina.lesinska@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">en@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">monika.drygulska@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">magda.b@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">robert.zadrozny@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">newsletteren@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">hakin9@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">romanp@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">tonid@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">en@hakin9.org<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: .0001pt; margin-bottom: 0cm;">
    </div>
    
    <div style="margin-bottom: .0001pt; margin-bottom: 0cm;">
    </div>
    
    <div>
      While this is a relatively modest list of emails, I hope that’s enough to show you theHarvester’s power and simplicity. Next, let’s think for a while about some other places we can find emails. Remember what a regular email looks like: it’s either <a href="mailto:fistname.lastname@client.com">fistname.lastname@client.com</a>, or <a href="mailto:flastname@client.com">flastname@client.com</a>, or <a href="mailto:firstnamel@client.com">firstnamel@client.com</a>. There are, of course, some companies that put more effort to obscure the real email of their staff behind some sort of <a href="mailto:firlastn@client.com">firlastn@client.com</a>by putting together pieces of first and last names of various lengths. But those cases are rare, so forget about it for now. In general, emails can be obtained from employees’ names, period. And where can we find those names? Of course, on social networks.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div>
      The social network of choice here is, of course, LinkedIn. Despite its recent security issues, LI remains a serious business communication tool and not only for recruiting as some people may think. Even with ‘basic’ account you can dig a lot of client’s employees there: just search for a company name and export the results form browser to an HTML file. After that, apply your knowledge of the client’s naming convention: how the real ‘human’ names are transformed to usernames by their IT administrators. Few minutes of grep’ing and regexp magic, and here you are with your list of <i>potential </i>usernames. I say potential, because at this point it’s your ‘educated guesses’ of usernames, nothing more. To use it effectively, you should verify it and the question is ‘how’?<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
      For this purpose Social Engineers have three good friends: VRFY, EXPN and RCPT. These are the commands of SMTP protocol that makes our rare emails cross the Internet in the flow of constant spam load. They do the following: VRFY literally verifies a given email or username, EXPN expands mailing lists, end RCPT admits that the recipient’s email is correct in the course of SMTP conversation. While the latter is vital for email systems functioning properly, the former two should not be used, especially on the Internet facing email servers, so called MXs. And the main reason why is that having access to these commands in the client’s domain we can easily verify every single guess we made about their usernames and emails. All these actions are easily automated by any <span style="font-family: &quot;Courier New&quot;; font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">netcat</span><span style="font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;"> </span>flavor and a scripting language like Perl or Python:<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">noroot@bt:~$ ncat mail.client.com 25<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">220 mail.client.com ESMTP; Wed, 12 Aug 2012 00:00:00 +0200<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">VRFY accounting <o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">250 Yeah, I know that one.&nbsp; He (or she) is Accounting Department <accounting client.com="client.com">.<o:p></o:p></accounting></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">VRFY vpupkin<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">250 Yeah, I know that one.&nbsp; He (or she) is Vasiliy Pupkin <vpupkin client.com="client.com">.<o:p></o:p></vpupkin></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">quit<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;">221 See ya in cyberspace<o:p></o:p></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
      <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; mso-bidi-font-size: 11.0pt;"><br /></span>
    </div>
    
    <div style="margin-bottom: 0.0001pt;">
    </div>
    
    <div>
      Yeah, see ya. Thanks for making my day.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
      As you can see, even a small organizations leek all sort of contact information to the public. And the main reason is because almost none or of them treats this type of information with due respect. But Social Engineers do.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
      Another place to search for contact details is… your client’s website. And I don’t mean those contacts on ‘About’ page which you should have found in very beginning. Instead, search for some office documents and PDF files. For that use a Google ‘dork’ of this kind: <span style="font-family: &quot;Courier New&quot;; font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">site:hakin9.org filetype:pdf</span><span style="font-size: 10.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;"> </span>and you can combine various file types joining them by OR keyword. There are always such files, because your client’s business should use some documents. And documents usually contain Metadata.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div>
      Metadata’s definition is tricky: it’s data about data. Roughly speaking, it is not what’s contained within the document, although that information can also be very interesting, but rather what are the properties of the document itself. These properties might be document’s name, location, revision number, size, or, and that is of most interest to us, its author. Document’s author usually is the operating system username that created it, which leads us to a new contact to verify and then send our emails. All this data can be seen in the document’s properties once it’s downloaded from the website, however doing this manually is kind of boring. And since the metadata has its value, it should come with no surprise that there is a tool for its collection.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
      Meet FOCA: the ultimate metadata mining tool. It searches websites for documents that contain metadata and then downloads them, parses them for information, and then categorizes and correlates what it’s found. Along with contact information, there are more sweets for you: the types and versions of software by which the documents have been created. You can download FOCA following a short registration process on its website <a href="http://www.informatica64.com/foca.aspx">http://www.informatica64.com/foca.aspx</a>.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
    </div>
    
    <div>
      So, let’s start FOCA and create a sample project using <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">docstoc.com</span> domain website. The first thing you will see is the search windows. You can choose from one to three of supported search engines there and also limit the search to specific types of documents. Although I believe it’s a good idea to always search with and for all of them, let’s start with <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">Google</span>, <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">.pdf</span>and <span style="font-family: &quot;Courier New&quot;; font-size: 9.0pt; line-height: 115%; mso-bidi-font-size: 11.0pt;">.doc(x)</span> for now. As of the time of this writing, FOCA found 10 PDF files at hakin9.org website, so let’s download them. Click the right mouse button at any document URL and choose “Download All”. Downloading all PDF files from a website may take a while, then click it again and choose “Extract All Metadata”. Warning: be careful with the files you’re downloading, because running malicious PDFs in vulnerable software may cause all sorts of harm.<o:p></o:p>
    </div>
    
    <div>
    </div>
    
    <div>
      <div style="clear: both; text-align: center;">
        <a href="http://4.bp.blogspot.com/-TJ3vxUkmFTk/UD0i1rBysvI/AAAAAAAATs8/Py6-goRDG_o/s1600/Figure1.jpg" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="237" src="http://4.bp.blogspot.com/-TJ3vxUkmFTk/UD0i1rBysvI/AAAAAAAATs8/Py6-goRDG_o/s400/Figure1.jpg" width="400" /></a>
      </div>
    </div>
    
    <p>
      <div style="text-align: center;">
        Figure 1. The list of downloaded and analyzed documents in FOCA.
      </div>
      
      <div style="text-align: center;">
        <o:p></o:p>
      </div>
      
      <p>
        Once you’ve downloaded all the documents and extracted metadata from them, you will see that the tree of parameters in the left pane of FOCA’s windows is now populated with various values, including usernames and types and versions of software packages used to create the files. All this information is linked to the original files, so you can always find which user created what and by what software. Now you can go search for some folks still using Office XP and Adobe Reader 8. 
        
        <div>
          <o:p></o:p>
        </div>
        
        <div>
        </div>
        
        <div>
          Of course, it is completely up to us what amount of metadata leaks in the documents we create. Windows users can remove any detail of all of them at once just by opening the document’s file properties, going to ‘Details’ tab and clicking ‘Remove Properties and Personal Information’.<o:p></o:p>
        </div>
        
        <div style="clear: both; text-align: center;">
          <a href="http://1.bp.blogspot.com/-3xq_ioi9ZrY/UD0jFuAnwdI/AAAAAAAATtE/KPoAvh1rLx8/s1600/Figure2.jpg" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="400" src="http://1.bp.blogspot.com/-3xq_ioi9ZrY/UD0jFuAnwdI/AAAAAAAATtE/KPoAvh1rLx8/s400/Figure2.jpg" width="329" /></a>
        </div>
        
        <div style="text-align: center;">
        </div>
        
        <div style="text-align: center;">
          Figure 2. Edit or remove metadata from document files in Windows.<o:p></o:p>
        </div>
        
        <p>
          Unfortunately, things are not that simple for OpenOffice users and on Linux, but you can find the way to remove metadata by researching this topic yourself. If you are concerned about the security implications of metadata leakage in the corporate world (and I assume that you already are) you may also search online for some commercial-grade gateway-like software products.
        </p>
        
        <div>
          The next piece of software I want to show you has become an irreplaceable tool in the pentesters’ arsenal and Social Engineers are not the exception. Cool guys at Paterva created Maltego for our fun and profit. To describe what it does I will use one word: Magic. Of course, any IT magical trick has a piece of prominent technology behind it, in this case it’s an outstanding extendable information correlation engine, but anyway, Magic is the right word. You can download a Community Edition version of Maltego here <a href="https://www.paterva.com/web5/client/community.php">https://www.paterva.com/web5/client/community.php</a>, it also comes with the latest version of BackTrack. To start using Maltego you have to register on community website and resolve a captcha in its user interface once in a while. That is to remind you that you should definitely buy a fool version once you decide to use Maltego for your pentesting engagements.
        </div>
        
        <div>
        </div>
        
        <p>
          <span style="line-height: 115%;"><span style="font-family: inherit;">Alright, let’s start Maltego and create a new graph. Maltego calls its projects ‘graphs’ and you will soon know why.</span></span><br /><span style="line-height: 115%;"><span style="font-family: inherit;"><br /></span></span> 
          
          <div style="clear: both; text-align: center;">
            <a href="http://2.bp.blogspot.com/-mzqwmgD9Ols/UD0jb7gkCaI/AAAAAAAATtM/QsiuqGPLS8k/s1600/Figure3.jpg" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="266" src="http://2.bp.blogspot.com/-mzqwmgD9Ols/UD0jb7gkCaI/AAAAAAAATtM/QsiuqGPLS8k/s400/Figure3.jpg" width="400" /></a>
          </div>
          
          <p>
            <div style="text-align: center;">
              Figure 3. The list of Maltego transforms available for an email address.<o:p></o:p>
            </div>
            
            <p>
              At the left pane of the GUI you can see a list of various types of information you can insert into the graph. Think of these objects as ‘nodes’. Once put into the graph, every node can be ‘transformed’ into another type of object by a predefined transformation – either executed remotely on a server or located locally at your hard drive. At the picture above you can see the list of transforms available for an email address. Start playing with Maltego using your personal information and trying to transform it to something else and I am sure you will be surprised with the results.
            </p>
            
            <div>
              As you can see, Maltego does little that could not be performed manually otherwise. Remember those VRFY scripts we made earlier? They totally can replace ‘Verify email address exists [SMTP]’ transform on emails. Theoretically, all these transforms could be done by hands through searching the Internet and finding relationships between different pieces of data. But given Maltego’s ease of use and intuitive approach to information search and correlation I cannot imagine my life without it any more.
            </div>
            
            <div>
            </div>
            
            <div>
              Although execution of Social Engineering attacks is somewhat beyond the topic of this article, I cannot miss a chance to give you some guidance on it. Let’s assume that I wrote this article for a reason and at this point you have gathered a list of valid email addresses of the client you have an engagement with. Let’s also assume that you have an explicit written permission to perform Social Engineering audit of your client’s organizational security controls and employee awareness. And it would also be great to ensure that your client have notified their employees that an audit may take place. (Yes, I know, that’s hard, but we cannot stay within ethical boundaries without all these precautions). In a situation like this you may start sending your emails and that is another area for automation.
            </div>
            
            <div>
            </div>
            
            <div>
              Social-Engineer Toolkit is your friend for that. SET comes with BackTrack or can be downloaded from its developer’s website <a href="https://www.trustedsec.com/">https://www.trustedsec.com/</a>. Dave ‘Rel1k’ Kennedy brought it to us so we can use that mighty tool to conduct an array of various SE attack scenarios. To run it <span style="font-family: 'Courier New'; font-size: 10pt; line-height: 115%;">cd</span><span style="font-size: 10pt; line-height: 115%;"> </span>to its work directory <span style="font-family: 'Courier New'; font-size: 10pt; line-height: 115%;">/petntest/exploit/set</span> and start it as root: <span style="font-family: 'Courier New'; font-size: 10pt; line-height: 115%;">sudo ./set</span>
            </div>
            
            <div>
              <span style="font-family: inherit; line-height: 115%;"><br /></span>
            </div>
            
            <div>
              <span style="font-family: inherit; line-height: 115%;">SET has a structured text-based interface organized as a tree of menus. Since we decided to work on two specific types of attacks (sending links and attachments) let’s check out what can SET help us with in this regard.</span>
            </div>
            
            <div style="clear: both; text-align: center;">
              <a href="http://1.bp.blogspot.com/-Bt6SPWIhNSg/UD0j3pMNLpI/AAAAAAAATtU/yK9EUxj0-gk/s1600/Figure4.jpg" style="margin-left: 1em; margin-right: 1em;"><img border="0" height="640" src="http://1.bp.blogspot.com/-Bt6SPWIhNSg/UD0j3pMNLpI/AAAAAAAATtU/yK9EUxj0-gk/s640/Figure4.jpg" width="441" /></a>
            </div>
            
            <p>
              <div style="text-align: center;">
                Figure 4. Social-Engineer Toolkit main menu.<o:p></o:p>
              </div>
              
              <p>
                By choosing ‘1) Social-Engineering Attacks’ menu item, you will see that first available options are exactly what we needed: ‘1) Spear-Phishing’ and ‘2) Website’ attack vectors. Spear-phishing lets us conduct either mass or directed email attacks with predefined email templates and recipients lists. SET has strong integration with Metasploit in order to handle the results of your attacks. Try to proceed with configuring a spear-phishing attack and you will see that there is a wide choice of payloads to attach to your email. Payloads can be configured to start and run various kinds of remote shells including Meterpreter, and there is a flexible configuration for how your shells should ring back home. From my experience, Java or PDF payload with Meterpreter reverse HTTPS shell works almost all the time. After choosing payload options, SET sends your emails and starts Metasploit reverse connection handler for you. All you have to do now is just sit and wait for Meterpreter sessions finding their way home. Be careful: since most social engineering attacks have extremely high success rate, your reverse handler may hang or crash under the DoS. Just kidding.
              </p>
              
              <div>
                Alright, what about credentials harvesting? Don’t erase all those email addresses, we’ll need them. Run Social-Engineer Toolkit once again and choose ‘1) Social-Engineering Attacks’, then ‘2) Website Attack Vectors’. Then choose attack method, Java Applet is my favorite for this vector, but you choose ‘2) Credential Harvester’. SET can start a web server for you and populate it either with a predefined template or a cloned site. Although cloned sites are extremely useful for social engineering attacks, they often cannot be used due to complexity of modern web applications. In these cases, when the website has a dynamic structure or its URL contains some personalized part that cannot be guessed by site cloner script, you will find Web Templates approach very useful. But for now choose ‘2) Site Cloner’ and clone some well-known website such as Twitter or Facebook. Social-Engineer Toolkit will now clone and start the website for you and you can direct your browser to <a href="http://localhost/">http://localhost</a> to see the exact copy of cloned website. Type some gibberish to sign-in form and submit it then go back to SET still running on background. As you can see, your browser is automatically redirected to the true cloned site, and your login credentials are showed in SET. Impressive, huh?
              </div>
              
              <div>
              </div>
              
              <div>
              </div>
              
              <div>
                Once again, as in the case with Maltego, you can see that this entire juicy staff can be done manually with little knowledge of any scripting language. But it would take so much time to automate social engineering attacks with such level of usability. So next time you meet Dave, buy him a beer. But be careful and don’t hug him!
              </div>
              
              <div>
                As you can see from above, there is a nice set of tools that can be used during a social engineering audit. Take them and put them to good use. I hope that information in this article can help you assess and increase security awareness of your colleagues and customers. But there is one more thing I want to stress here.
              </div>
              
              <div>
              </div>
              
              <div>
                Remember that you assess security, e.g. processes that help people and organizations manage the risk. Thus processes are the ones to blame here once you accomplish a huge success during the audit and indicate the ease of obtaining critical information or running a shell on a critical system. Many organizations do not understand that in this case processes fail, not people. And the cases when people pay for the lack of organization’s commitment to security are not rare.
              </div>
              
              <div>
              </div>
              
              <div>
                As a security auditor, you should always remember that firing a person who ‘clicked the link&#8217; is the stupidest action to take since this person is probably the most security aware employee when the audit ends and you present the report. So, first educate your customer in regard of the things said and then try to keep your results unbiased and remove all personal details from the report before sending it to your customer. These are things that save your karma and let you sleep at night.
              </div>
              
              <div>
              </div>
              
              <div>
                As a conclusion, as promised, let me present you with some direction for further research on the topic of Social Engineering. In this article we discussed the very technical part of the trade that constitutes a very small portion of social engineering knowledge. To know more, use an outstanding Social Engineering Framework at <a href="http://www.socail-engineer.org/">http://www.socail-engineer.org</a> and listen to its monthly podcast.&nbsp;Also, there is a great book written by Chris Hadnagy, the founder of social-engineer.org, called ‘Social Engineering, the Art of Human Hacking’ which I strongly recommend once you decide to know more on the topic.
              </div>
              
              <div>
                <o:p></o:p>
              </div>
              
              <div>
              </div>
              
              <div>
                This article <a href="http://hakin9.org/samuraiwtf-toolkit-exploiting-software-0712/?a_aid=nataliaboniewicz&a_bid=8f6377e8">originally appeared in Issue 7</a>, 2012, of <a href="http://hakin9.org/subscription/?a_aid=nataliaboniewicz&a_bid=8f6377e8">Hakin9 IT Security Magazine</a>
              </div>
              
              <div>
              </div>
              
              <p>
                </div> 
                
                <div class="addtoany_share_save_container addtoany_content_bottom">
                  <div class="a2a_kit a2a_kit_size_32 addtoany_list a2a_target" id="wpa2a_245">
                    <a class="a2a_button_facebook" href="http://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2Fmy-article-in-hakin9-magazine-issue-712%2F&linkname=My%20article%20in%20Hakin9%20magazine%20Issue%207%2F12" title="Facebook" rel="nofollow" target="_blank"></a><a class="a2a_button_twitter" href="http://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2Fmy-article-in-hakin9-magazine-issue-712%2F&linkname=My%20article%20in%20Hakin9%20magazine%20Issue%207%2F12" title="Twitter" rel="nofollow" target="_blank"></a><a class="a2a_button_google_plus" href="http://www.addtoany.com/add_to/google_plus?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2Fmy-article-in-hakin9-magazine-issue-712%2F&linkname=My%20article%20in%20Hakin9%20magazine%20Issue%207%2F12" title="Google+" rel="nofollow" target="_blank"></a><a class="a2a_button_linkedin" href="http://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fblog.styran.com%2F2012%2F08%2Fmy-article-in-hakin9-magazine-issue-712%2F&linkname=My%20article%20in%20Hakin9%20magazine%20Issue%207%2F12" title="LinkedIn" rel="nofollow" target="_blank"></a><a class="a2a_dd addtoany_share_save" href="https://www.addtoany.com/share"></a>
                  </div>
                </div>