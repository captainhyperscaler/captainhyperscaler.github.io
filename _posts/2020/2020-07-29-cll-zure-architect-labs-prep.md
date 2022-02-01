---
layout: post
title: So You want to be an Azure Solutions Architect Expert…the blog series...Labs and Exam Prep

---

<!-- wp:image {"align":"center","id":689,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/cll-azure-solution-architect-poster.jpg?w=1024" alt="" class="wp-image-689"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Welcome to this installment of the "So You want to be an Azure Solutions Architect Expert" series. This is the sixth accompanying article, and it will focus on some exam tips and lab focus areas that can help you in your final preparation to take the AZ-303 and AZ-304 exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To attend the session on Friday, July 31, 2020, please access the link for the <a rel="noreferrer noopener" href="https://www.cloudlunchlearn.com/" target="_blank">Cloud Lunch and Learn website</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These sessions are also being recorded and posted on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this session and article, I will be discussing some final steps to prepare for you exam experience. This includes how to prepare your testing location if you are taking this exam utilizing home proctoring, and how to use the Azure portal to prepare for the possibility of labs.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The topics that I will discuss on Friday include the following:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Exam preparation</strong>: Microsoft began utilizing home proctoring in 2019 for all of their role-based exams.  This exam delivery method allows you to utilize your own equipment from home or office, and avoids the need to travel to a testing facility.  This provides a level of convenience that I value when taking an exam.  The check-in and proctoring process with Pearson Vue has evolved quite a lot over the past 18 months, and it has become a pretty smooth process. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are some key points that you need to understand going into the exam.</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Check-in 30 minutes before your scheduled exam time.  This gives you a much less stressful experience.  You may wait for a proctor for up to 15 minutes (this has been the case for me one time, most of the time it is 5 minutes, tops.), and since Microsoft will expire an exam 15 minutes past the scheduled exam time, you don't want to be racing the clock.  Have your ID ready and the check-in will have you use your smart phone to take a picture of your ID and the room around your workspace.  Once check-in is complete, the proctor will either contact you for some final questions or will launch your exam.  This brings us to #2...</li><li>Make sure that ALL software running in background processes are stopped/ended.  This includes any anti-virus and anti-malware.  The Pearson Vue testing software has a tendency to be seen as malware and may crash when the exam is launched.  It seems that Pearson has taken note of this recently (or Microsoft Defender) as I have been prompted on my latest exams to Allow this software on my network.  Better safe than sorry, go into your task manager and end these processes... I also pause syncing of any cloud storage (OneDrive, Dropbox).  The Microsoft store and any running preloaded Xbox software has also given me trouble in the past.</li><li>Make sure that your workspace is clean.  You cannot have anything on the desk or table that you are taking the test.  They only want to see the device that you are taking the test.  This includes external monitors.  I have heard from others that with the work from home orders in many countries, that Pearson is allowing the external monitors but requires you to show that they are unplugged.  Personally, I use the kitchen table to take my exams to avoid any issues with my desk.</li><li>Where you pick and the time that you pick to take your exam is extremely important.  There must not be any sounds or sights of anyone else while you are taking your exam, or the proctor could end your exam.  Make sure that where ever you choose is free from interruptions.  With families home from work and school, it is important to let them know that they need to stay away from your camera area and to not talk to you while taking the exam.  In these situations, I choose to get up early before the family is expected to be up.  Which means that I've been scheduling my exams for 5 AM.  If you are back to work in an office, small conference rooms are a great option as well.  If there is a presentation monitor in these rooms, sit with it at your back and unplug it if you can.</li><li>This last point is very important.  Make sure that you have confidence in your device.  The webcam and microphone must be in working order for the proctor to release the exam.  When you schedule your exam for home proctor, there is a link to test your system to make sure that it works, I highly recommend doing this before scheduling your first home proctor exam and run this pre-test the day before your exam to verify that everything is in proper working order.  Be sure to run this test on the same network that you will be logging into to take the test.</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>Exam question format</strong>: When I'm doing a training for a Microsoft exam, I often get asked what the questions are like on the exam.  There are generally six types of questions that you can expect on the exam.</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>The first of these is the typical <strong>multiple choice</strong>, where there is a scenario given with requirements and you need to make the proper selection.  This could be a single selection or multiple selections.  If it is multiple selections, Microsoft does generally tell you how many choices to select and the testing engine will not let you move forward without selecting the proper number of answers.</li><li><strong>Case study</strong> questions are a major part for many of the role-based exams.  That is the case for the Solutions Architect exams as well. You can expect a few of these, especially for the AZ-301/304 exam since it is based on design.  These questions provide an organizations current situation, their current technological environment, and then what they are wanting to accomplish in Azure.  You will be given anywhere from 4 to 8 questions on these case studies, usually multiple choice questions.</li><li><strong>Drag and drop</strong> questions are the next type that I want to bring up.  As with most of the Microsoft questions, they start with a scenario and business requirements.  The question then asks you to accomplish these requirements "in order" by moving the steps into place from the selections on the left to an area on the right.  Like the multiple choice questions, it will tell you specifically how many steps are needed and the test engine will not allow more selections to be moved into the answer area than what is required.  When preparing for an exam, if you are using a training guide or Microsoft Learn, make note of any content that has numbered steps and study the order of these steps.  This will help you with this type of questions.</li><li><strong>Drop-down selections </strong>to complete missing code are the next.  Microsoft does not require you to know PowerShell and CLI from a blank canvas of writing code, but it is necessary that you understand the structure of these commands and how to complete commands properly.  These questions provide lines of code with missing variables that contain a drop-down with potential options to complete the command that is based on the question.  Knowing how commands work within PowerShell and CLI will make you successful with these questions.</li><li><strong>Yes/No</strong> questions are based on a scenario and usually an exhibit showing a configuration screenshot from the portal.  There will then be three statements that you are asked to answer whether they are correct or not by selecting "Yes" or "No".</li><li>The last question type is the trickiest of the all of these.  I call these <strong>scenario-based questions</strong>.  You will be warned going into these questions that you will be given a series of questions and once you answer the question you can not go back.  What these questions do is they provide a specific scenario and then a proposed solution to the scenario.  You are then asked if this solution solves the requirements.  This truly tests your understanding of Azure services, because you will be given 3-4 options in a row for to solve the scenario.  If you select one of the earlier options and find that that was incorrect and the next solution was the correct one, you cannot go back to correct.</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>One final statement on the exam questions.  Answer ALL of the questions.  Don't skip any.  You are not marked down for wrong answers, so skipping a question gives you nothing while taking a guess may give you points.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Lab preparation</strong>: The Microsoft Learning github repository contains lab guides that can be used to prepare for any exam: <a rel="noreferrer noopener" href="https://github.com/MicrosoftLearning" target="_blank">https://github.com/MicrosoftLearning</a>.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Some key areas to focus on will be discussed on Friday's session.  The primary areas to focus in my eyes would be the labs within github that mirror the Microsoft Official Course content.  I also recommend practicing the following:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For AZ-300/303:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Creating a virtual machine, virtual machine scale set, and attaching   disk storage</li><li>Creating VNETs and peering multiple VNETs.  Also, working with NSGs to create rules</li><li>Creating storage accounts, particularly BLOBs/Containers and File  shares</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>For AZ-301/304:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Steps required to initiate an Azure Migrate project</li><li>Steps for setting up Azure Site Recovery</li><li>Understanding how to move data to Azure. This includes Storage Explorer, AZcopy, and creating Import/Export jobs</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>These topics will be covered in my Cloud Lunch and Learn session on Friday, July 31, 2020. The recording will be located on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional links to assist in initial preparation include:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Cloud Lunch and Learn <a rel="noreferrer noopener" href="https://github.com/Cloud-Lunch-and-Learn/Cloud-Lunch-and-Learn-Sessions" target="_blank">github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Build5Nines self-assessment tools: <a rel="noreferrer noopener" href="https://build5nines.com/free-oss-exam-self-assessment-tool/" target="_blank">https://build5nines.com/free-oss-exam-self-assessment-tool/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microsoft Learn: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-300?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-300</a> and <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-301?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-301</a> on-demand training</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>AZ-303 labs on github: <a rel="noreferrer noopener" href="https://github.com/MicrosoftLearning/AZ-303-Microsoft-Azure-Architect-Technologies" target="_blank">https://github.com/MicrosoftLearning/AZ-303-Microsoft-Azure-Architect-Technologies</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>AZ-304 labs on github: <a href="https://github.com/MicrosoftLearning/AZ-304-Microsoft-Azure-Architect-Design" target="_blank" rel="noreferrer noopener">https://github.com/MicrosoftLearning/AZ-304-Microsoft-Azure-Architect-Design</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Greg posts Microsoft Docs links for every exam objective here: <a rel="noreferrer noopener" href="https://github.com/gsuttie/AzureResources/tree/master/Exams" target="_blank">Gregor Suttie github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Pixel Robots is a helpful source of information, especially for AKS: <a rel="noreferrer noopener" href="https://pixelrobots.co.uk/" target="_blank">https://pixelrobots.co.uk/</a></p>
<!-- /wp:paragraph -->