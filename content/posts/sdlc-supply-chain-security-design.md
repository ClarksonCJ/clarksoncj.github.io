+++
date = 2024-08-30T06:00:00Z
publishDate = 2024-08-30T06:00:00Z
title = "Software Supply Chain Security in the SDLC: Design Phase"
slug = "supply-chain-sdlc-security"
tags = [
  "Secure Design",
  "Supply Chain Security",
  "Secure SDLC",
  "Designing for Security",
  "Holistic Security"
]
categories = ["Posts"]
thumbnail = "/images/secrets-management.png"
description = "Consider the security of your supply chain as a holistic view of your SDLC, starting with solutions design"
draft = false
showDate = "true"
showToc = true
TocOpen = false
hidemeta = false
comments = false
disableShare = false
disableHLJS = false
hideSummary = false
searchHidden = true
ShowReadingTime = true
ShowBreadCrumbs = true
ShowPostNavLinks = true
ShowWordCount = true
ShowRssButtonInSectionTermList = true
UseHugoToc = true
+++

In the wake of high-profile security breaches like Log4Shell, CodeCov, and OrionGate, software supply chain security has surged to the forefront of industry concerns. These incidents have driven remarkable advancements in technology aimed at fortifying our supply chains. Yet, despite these leaps forward, some critical areas remain under-addressed, often because they require a more holistic and integrated approach rather than standalone solutions.
Discussions about software supply chain security often center on topics like SBOMs, dependency management, and open-source risks. While these concepts are fundamental and addressing them offers substantial benefits, they don't cover the entire landscape. There are other crucial facets of the Software Delivery Lifecycle that frequently go unnoticed when it comes to supply chain security.
Today, we will delve into two fundamental areas of software delivery; the what, and the how, discussing strategies for enhancing supply chain security in each. By adjusting our view on the usual topics, we can build a more robust and resilient security framework that protects us as both as a consumer, and producer in the software supply chain.

# Design - What are you going to build?

Well-architected software design incorporates security principles from the ground up, making it inherently more resilient to attacks. By adopting secure design practices such as threat modelling, defense in depth, and secure coding standards, developers can minimize potential vulnerabilities that attackers might exploit.
Secure design practices extend beyond your code - they encompass the entire software supply chain. The principles of the Security Triad - Confidentiality, Integrity, and Availability - are just as critical here. Ensuring the availability of packages, container images, and tools for your engineers means that your development process remains uninterrupted and efficient. If these resources become unavailable, it can halt your development pipeline and delay critical updates and features.
Integrity is equally vital. The integrity of your packages, images, and tools must be maintained to prevent upstream compromises from infiltrating your system. A breach in any of these components can have cascading effects, potentially introducing vulnerabilities into your software. Implementing robust verification processes, such as cryptographic checksums and digital signatures, helps ensure that what you receive is exactly what was intended.
Lastly, the confidentiality of the data processed by your solution hinges on your implementation and technology choices. Secure design must consider how data is handled, stored, and transmitted to prevent unauthorized access. Encryption, access control, and secure coding practices all play a part in safeguarding sensitive information. However, the effectiveness of these data protection strategies is only as strong as the handling of the cryptographic materials in the supply chain. Proper management of keys, credentials, and other sensitive information is crucial. Ensuring that these elements are securely exchanged and stored supports robust and resilient secrets management, which is vital for maintaining the confidentiality of your data.
Threat models are an invaluable tool for assessing your design and proactively managing project risks. This extends beyond evaluating individual features to encompass the entire supply chain. Such as when you need to incorporate new third-party dependencies or containers to meet your feature requirements, it's crucial to consider the confidentiality, integrity, and availability of these components within your supply chain.
Integrating a supply chain threat model into your overall software threat modeling process allows you to adjust your design and implementation to mitigate risks early, before they become more significant and costlier to address. This approach not only enhances your security posture but also embeds security into the very fabric of your development process.
By embedding these secure design principles into your software supply chain, you not only protect your product but also build a resilient foundation that can withstand and quickly recover from potential security incidents. This proactive stance ensures that security is not just an add-on but a core component of your software development lifecycle.

# Process - How are you going to build it?

Security, especially supply chain security, must be embedded into your software delivery methodology from the start. Think of your solution as a link in the broader supply chain - how you secure it will have lasting effects throughout your entire delivery pipeline. If security is treated as an afterthought or kept separate, it won't be prioritized, and the pressure to "ship it" will always override security concerns.
From my experience, this is a compelling reason why the security engineering team should not live outside the core engineering organisation. When security engineers sit at the same table as software engineers, sharing the same delivery goals, security naturally becomes a part of the delivery objectives. This collaborative approach ensures that critical security measures are implemented, even if not every security request is fulfilled. By being in the trenches together, security and engineering teams can balance the urgency of deadlines with the necessity of robust security practices, leading to a more secure and reliable software delivery pipeline.

## Embedding Security Engineers into Engineering Teams

1. Integrated Teams: Security engineers should be embedded directly within engineering teams working on critical projects. This integration means they participate in all stages of the development lifecycle - from planning and design to implementation and testing.
2. Shared Goals and Objectives: Align security goals with project goals. Security engineers should be involved in setting project objectives, ensuring that security considerations are part of the initial planning stages and not added as an afterthought.
3. Regular Communication and Collaboration: Facilitate regular meetings and communication between security and engineering teams. This can be achieved through daily stand-ups, sprint planning, and retrospectives where security implications are discussed alongside other project aspects.
4. Security Champions: Identify and train security champions within each engineering team. These individuals act as liaisons between the security team and the rest of the engineering team, promoting security best practices and ensuring that security remains a priority.
5. Integrated Tools and Processes: Utilize tools that integrate security checks into the development pipeline. Automated security testing, code analysis, and dependency scanning should be part of the CI/CD pipeline, allowing security issues to be identified and addressed early in the development process.
6. Joint Training and Education: Conduct joint training sessions and workshops where both security and engineering teams can learn about the latest security threats, tools, and best practices. This helps build a shared understanding and a culture of security-first thinking.

## Benefits of Embedded Security Engineers
1. Proactive Security: By involving security engineers from the outset, potential vulnerabilities can be identified and mitigated early, reducing the risk of security issues arising later in the development process.
2. Enhanced Collaboration: Integrated teams foster a culture of collaboration and shared responsibility. Security becomes a collective goal rather than a separate concern, leading to more cohesive and effective teams.
3. Faster Response to Threats: With security engineers embedded in the team, the response to emerging threats or vulnerabilities is faster and more efficient. Issues can be addressed in real-time, minimizing potential damage and disruption to delivery goals.
4. Balanced Priorities: Security engineers working alongside software engineers help balance the need to meet deadlines with the necessity of maintaining strong security practices. This balance ensures that critical security measures are not overlooked in the rush to deliver.
5. Improved Quality and Reliability: Embedding security into the development process leads to higher quality and more reliable software. Security considerations are built-in, resulting in fewer vulnerabilities and a more robust end product.

By embedding security engineers into your engineering teams, you not only enhance your security posture but also create a more integrated, collaborative, and efficient development process. This approach ensures that security is a foundational element of your software delivery pipeline and by extension your place in the broader supply chain, leading to safer and more resilient software products.

# Bringing It All Together

An interesting quote I came across recently has stuck in my head as I considered this post: "How you do anything is how you do everything." There are variations on the quote and how it's explained, but the crux of the idea is that the habits and patterns you form transfer to everything you do. For example, If you work hard at one thing, you are likely to transfer that energy to other areas of your life.
In the context of software design and the delivery process, especially when viewed from the lens of securing the supply chain, this suggests that leveraging secure design principles during the design phase will ensure these principles persist throughout the Software Development Life Cycle (SDLC). If you embed security practices like threat modelling, secure design principles, defence in depth, etc. early and consistently, they become a natural part of your workflow, enhancing the overall integrity, confidentiality, and availability of your software.
By making security a fundamental part of your development process, not an afterthought, you build stronger, more resilient systems. This proactive approach not only protects your software from potential supply chain attacks but also instills a culture of security within your teams. Remember, the effort you put into securing your software today will pay dividends in the long run, ensuring a robust, reliable, and secure software delivery pipeline.
So, next time you're mapping out a project or sprint, think about how you can integrate security into every step. Because, after all, how you secure anything is how you secure everything.