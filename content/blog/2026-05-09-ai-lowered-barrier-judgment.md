+++
title = "AI Lowered the Barrier, But It Did Not Replace Judgment"
date = 2026-05-09T00:00:00-04:00
slug = "ai-lowered-barrier-judgment"
summary = "AI makes generation cheaper, but it does not replace the human judgment needed to define problems, review plans, and decide what is actually worth shipping."
tags = ["AI", "Workflow", "Judgment"]
+++

<div class="bilingual-post" data-title-en="AI Lowered the Barrier, But It Did Not Replace Judgment" data-title-zh="AI 降低了门槛，但没有替代判断">
<div class="language-toggle" role="group" aria-label="Article language">
<button class="language-toggle__button is-active" type="button" data-language-target="en" aria-pressed="true" aria-controls="article-en">English</button>
<button class="language-toggle__button" type="button" data-language-target="zh" aria-pressed="false" aria-controls="article-zh">中文</button>
</div>

<div id="article-en" class="bilingual-body" data-language="en" lang="en">
<p>A few days ago over lunch, I was talking with a friend about how people are actually using AI now.</p>
<p>The topic itself is already very normal. Who does not use AI now? We use it to write code, write documents, make plans. It almost feels strange not to talk about AI. But in the middle of the conversation, he asked me a very interesting question:</p>
<p>How many tokens did you use?</p>
<p>I paused for a second.</p>
<p>It is not that tokens do not matter. Of course they matter. They are cost, and they are also the budget of the context window. But if we start using “how many tokens did you use” as a metric for whether someone is good at using AI, I think something starts to go wrong.</p>
<p>Because tokens are very easy to waste. You can let AI keep running, keep generating, keep saying the same thing in different ways. You can also let it go further and further in the wrong direction, making that direction look more complete and more convincing. But none of that means the work is actually moving forward.</p>
<p>The real question should not be how many tokens were used. The real question is whether the problem was solved. Did the code run? Was the plan reviewed? Did the tests pass? Can the result actually be shipped?</p>
<p>This distinction sounds simple, but I feel like it is becoming easier and easier to forget in the current AI hype cycle.</p>

<h2>A Lower Barrier Is Not the Same as Production Ability</h2>
<p>In the past few months, everyone has been saying that AI lowered the barrier.</p>
<p>I agree with that. AI did lower the barrier. In the past, you might have needed to study for a long time before you could build a demo. Now, if you can describe what you want, AI can help you put something together very quickly. This is true for coding. It is true for video. It is true for advertising.</p>
<p>But the problem is: a lower barrier does not mean production-level ability suddenly appears.</p>
<p>For example, many people now say AI video is here, AI ads are here, and these things can just be generated directly. But the more I use AI, the more I feel that this is not how it works. If you want to use AI to make a watchable ad, it is not enough to type one prompt. You still need to understand how to write a script, how to arrange shots, how pacing works, what kind of image is effective, and what kind of expression is empty.</p>
<p>Code is the same. AI can quickly help you write a feature, but you still need to know why the feature is written this way, how it works with the rest of the system, where it might break, how it should be tested, and whether it will affect users after deployment.</p>
<p>So AI is more like an accelerator. It is an amplifier. It is not something that replaces professional ability from zero to one.</p>
<p>It amplifies the judgment you already have. If you know what good looks like, it can help you get there faster. If you do not know what good looks like, it can also quickly generate a pile of things that look like progress.</p>
<p>That is the part people can easily misread.</p>
<p>Before, if someone did not know how to do something, they often simply could not make it. Now, even if someone does not know, they can still make something. The real question is whether that thing is a toy, or whether it can actually live in a real production environment. The gap between those two is huge.</p>

<h2>Context Is the Actually Scarce Resource</h2>
<p>I used to really like large context windows.</p>
<p>Honestly, when I first had the freedom to use them, it felt great. You could throw in a bunch of files, background, thoughts, and let AI keep running. It looked like it knew everything and could connect everything.</p>
<p>But later I slowly realized that a large context window does not only bring benefits. It also brings noise.</p>
<p>After a long conversation runs for a while, it accumulates old assumptions, wrong directions, and context that has technically been overturned but has not fully disappeared. On top of that, context compression itself loses information. So you think the model still remembers the full thing, but what it actually remembers is a compressed and polluted version of the thing.</p>
<p>Then it keeps moving forward based on that version.</p>
<p>This is especially obvious in coding. One agent writes code, reviews its own code, tests its own code, and then explains why what it did is right. It sounds automated, but it can easily become self-reinforcement.</p>
<p>So later I started caring much more about context hygiene.</p>
<p>Now I prefer to write a plan first, or a requirement document. The main agent should not do everything. It should act more like a PM, only caring about direction, status, and task breakdown. The worker that writes code should be separate. The reviewer should be separate. The tester should also be separate.</p>
<p>This is not for showing off. It is not because “multi-agent workflow” sounds fancy. For me, its most important value is isolation.</p>
<p>The implementer only looks at what needs to be implemented. The tester only looks at how to verify it. The reviewer tries to look at the work from another angle and find what is wrong. The main agent does not need to eat all the noise. It only keeps the plan and final state.</p>
<p>That is more stable.</p>
<p>Sometimes external constraints force you to build a better system. When the context window was huge, I was more likely to throw everything into it. When the window became less free, I was forced to think: what should go in, what should be isolated, and what should be passed through files and plans instead of being stuffed into one chat?</p>
<p>The final result was actually better.</p>

<h2>The Biggest Risk of AI Is Not That It Is Dumb. It Is That It Agrees Too Well.</h2>
<p>The thing that scares me most about AI now is not whether it writes bad code.</p>
<p>Bad code is manageable. You can test it, run it, look at errors, and review it.</p>
<p>The harder problem is that AI is too good at going along with you.</p>
<p>For example, in my work on SafeClick, I stepped into this trap. The first version of the plan had problems, and later I came up with a second version. When I took my own plan and asked AI about it, it helped me explain the plan very completely and very reasonably. Everything seemed to make sense.</p>
<p>But later, when I changed the framing and asked it to review the same plan from the angle of “this plan may have problems,” it could point out a long list of issues.</p>
<p>That is scary.</p>
<p>Because it means AI is not always standing in a stable, objective review position. A lot of the time, it is responding to your framing. If you ask, “What do you think of my plan?”, it tends to help strengthen it. If you ask, “Does this plan have problems?”, it tends to help find problems.</p>
<p>If you do not realize this, you might think AI is giving you objective judgment. But in reality, it might be giving you emotional value.</p>
<p>And this emotional value is subtle. It is not just saying, “You are great.” It uses very professional language to make your idea look more complete, making you feel more and more confident that your direction is correct. You see it generate so much content, so much analysis, so many reasons, and it becomes easy to think: if it can explain it this completely, then it must be right.</p>
<p>But completeness is not correctness.</p>
<p>Sometimes the thing that breaks this wrong path is a real person directly telling you: this plan does not work.</p>
<p>That kind of feedback may not sound nice, but it is useful. It does not need to agree with you, and it does not need to make the conversation comfortable by wrapping the problem in soft language. It pulls you out of that self-reinforcing path directly.</p>
<p>This is also why I believe less and less in the story that “one person plus a bunch of AI agents can solve everything.”</p>
<p>It is not that one person cannot do a lot. AI really does make one person much stronger. But if the entire system is just you and a group of AIs that are good at agreeing with you, then your own cognitive bias can also be amplified many times.</p>
<p>If one AI says you are right, you may still doubt it. But if three, five, or ten AIs all help you make the same wrong direction sound reasonable from different angles, you may really start believing that you are right.</p>
<p>That part is dangerous.</p>

<h2>Market Narratives Also Agree Too Well</h2>
<p>There is also a bigger problem: it is not only AI that agrees with you. The market tells stories too.</p>
<p>Right now, many AI narratives are very strong. A model comes out, and people say it will replace a certain number of jobs. A company publishes a report, and everyone starts to panic. A product becomes popular for coding, and people start assuming it is the only correct answer.</p>
<p>But how much of this is real capability, how much is marketing, and how much is the story the capital market wants to hear? These things need to be separated.</p>
<p>I am not saying these companies are bad. I am not saying AI has not changed the world. AI has absolutely changed my workflow. I use it every day, and I use it a lot. It really helps me work faster, and it lets me do things that would have been hard to finish alone before.</p>
<p>But precisely because I actually use it, I feel even more strongly that we cannot treat marketing as reality.</p>
<p>Model companies have their interests. Executives have their stories. The market has its emotions. Everyone is saying “AI will do this” and “AI will do that,” but when you actually sit down to build something, the question is still very simple:</p>
<p>Who is making the judgment?</p>
<p>Who is defining the problem?</p>
<p>Who is deciding whether this thing can actually ship?</p>
<p>Who is responsible for the result?</p>
<p>The answer is still people.</p>
<p>AI can help you write, search, generate, and reason. But direction, tradeoffs, and responsibility cannot be outsourced.</p>

<h2>Do Not Mistake Chasing Hype for Learning</h2>
<p>This leads to another feeling I have had more and more recently: a lot of AI learning is fake learning.</p>
<p>Every day there are new tools, new models, new workflows, new skills. You feel like if you do not read about them, you are falling behind. If you do not try them, you are missing something. This kind of FOMO is very easy to fall into.</p>
<p>But seeing a lot of things does not mean you actually understand anything.</p>
<p>Sometimes you are only getting the feeling that “I am learning.” You collect many tools, download many skills, read many articles about how other people use AI. And then what? When you return to your own work, the real problem is still not solved.</p>
<p>I now prefer to start from the problem.</p>
<p>It is not that new tools should not be tried. They can be tried. But they should not become part of your workflow from day one. Wait until you really run into a repeated problem, then ask whether a tool can help solve it. Wait until you see a process repeat many times, then turn it into a skill.</p>
<p>A skill should originally be something distilled from your own workflow. It is not a plugin system where installing more things automatically makes you stronger.</p>
<p>Other people’s skills can be useful references, but copying them directly comes with a lot of water weight. They are answers to someone else’s problems, and they contain a lot of context that only fits that person. If you take them directly, you may just be adding friction to yourself.</p>
<p>The useful things should grow out of your own work.</p>
<p>You keep doing something and notice that one step repeats again and again. You step into a pit and realize that next time you must check something first. You review a few times and notice one type of issue is always missed. A process distilled at that moment is actually valuable.</p>

<h2>In the End, It Still Comes Back to Human Judgment</h2>
<p>So after going around in a circle, my view of AI is actually simpler than before.</p>
<p>AI is strong. It is really strong. It lowered the barrier, amplified ability, and changed many workflows.</p>
<p>But it did not replace judgment.</p>
<p>It lowered the cost of starting, not the cost of doing something well. It made generation cheap, but it also made wrong directions easier to package. It let one person do more, but it can also amplify one person’s cognitive bias. It made learning resources more abundant, but it also created a lot of fake learning.</p>
<p>So the most important ability in the AI era may not be how many tools you know, or how many tokens you can burn.</p>
<p>What matters more is whether you can define the problem. Whether you can see what is wrong with a plan. Whether, when AI agrees with you, you can pause and ask: is it judging objectively, or is it just responding to my framing? Whether, when the market narrative is loud, you can return to your own real work and ask whether this thing actually solves a problem.</p>
<p>The most valuable thing about AI is not that it replaces my judgment.</p>
<p>The most valuable thing about AI is that it amplifies what I have already judged clearly.</p>
<p>If my direction is clear, it makes me faster. If my direction is wrong, it may also make me wrong faster.</p>
<p>That is why, the deeper we go into the AI era, the more I feel human critical thinking matters.</p>
<p>Not less.</p>
<p>More.</p>
<p>Because generation is no longer scarce.</p>
<p>Judgment is scarce.</p>
</div>

<div id="article-zh" class="bilingual-body" data-language="zh" lang="zh-Hans" hidden>
<p>前几天午餐，我跟一个朋友聊天，聊到现在大家到底是怎么用 AI 的。</p>
<p>这个话题本身已经很普通了。现在谁不用 AI？写代码用，写文档用，做 plan 用，好像不聊 AI 反而不正常。但是他中间问了我一句很有意思的话：</p>
<p>你用了多少 token？</p>
<p>我当时有点愣住。</p>
<p>不是说 token 不重要。token 当然重要，它是成本，也是 context window 的预算。但是如果把“用了多少 token”当成一个人 AI 用得好不好的指标，我觉得这个地方就开始有点不对了。</p>
<p>因为 token 太容易被浪费了。你可以让 AI 一直跑，一直生成，一直把一个东西换一种方式再说一遍。你也可以让它在一个错的方向上越写越多，越写越完整，最后看起来非常像那么回事。但问题是，这些都不代表事情真的往前走了。</p>
<p>真正应该看的不是用了多少 token，而是这个问题有没有被解决。代码有没有跑起来，方案有没有被 review，测试有没有过，结果能不能交付。</p>
<p>这个区别看起来很简单，但是我发现，在现在这个 AI 热潮里，它反而越来越容易被忘掉。</p>

<h2>低门槛不等于生产级</h2>
<p>这几个月大家都在说，AI 降低了门槛。</p>
<p>这个说法我同意。AI 确实降低了门槛。以前你可能要学很久才能做一个 demo，现在你只要会描述需求，就能很快让它帮你搭一个东西出来。写代码是这样，做视频是这样，做广告也是这样。</p>
<p>但问题是，门槛降低了，不代表生产级能力就出现了。</p>
<p>比如说现在很多人说，AI 视频来了，AI 广告来了，以后这些东西都可以直接生成。但我越用越觉得，根本不是这样。你想用 AI 做一个能看的广告，不是只输入一句 prompt 就行了。你还是要知道脚本怎么写，镜头怎么安排，节奏怎么走，什么样的画面是有效的，什么样的表达是空的。</p>
<p>代码也是一样。AI 可以很快帮你写出一个功能，但你要知道这个功能为什么这么写，它跟系统里的其他部分怎么配合，哪里可能出错，测试应该怎么做，上线之后会不会影响用户。</p>
<p>所以 AI 更像是 accelerator。它是放大器，加速器，不是一个从 0 到 1 替代专业能力的东西。</p>
<p>它会放大你已经有的判断。如果你知道什么是好，它可以帮你更快地做出好东西。如果你不知道什么是好，它也可以很快帮你生成一堆看起来像成果的东西。</p>
<p>这才是最容易让人误判的地方。</p>
<p>因为以前一个人不懂，他可能做不出来。现在一个人不懂，他也能做出来一些东西。问题是，那些东西到底是玩具，还是能放到真实环境里的产品，这中间差得非常远。</p>

<h2>context 才是真正稀缺的东西</h2>
<p>我以前也很喜欢大的 context window。</p>
<p>说实话，刚开始能放开用的时候是很爽的。你可以把一堆文件、一堆背景、一堆想法全塞进去，然后让 AI 一直 run。它看起来好像什么都知道，什么都能接上。</p>
<p>但是后面我慢慢发现，大 context window 不一定只带来好处。它也会带来噪音。</p>
<p>一个长对话跑久了以后，里面会积累很多旧的假设、错误的方向、已经被推翻但还没有完全消失的上下文。再加上 context compression 本身也会丢信息，所以你以为它还记得完整的事情，其实它记住的是一个被压缩过、被污染过的版本。</p>
<p>然后它就会在这个版本上继续往下走。</p>
<p>这件事在 coding 里特别明显。一个 agent 一边写代码，一边自己 review，一边自己测试，一边自己解释为什么它做得对。听起来很自动化，但其实很容易变成自我强化。</p>
<p>所以后来我反而开始更在意 context hygiene。</p>
<p>我现在更喜欢先写 plan，或者写一个 requirement document。主 agent 不要什么都干，它更像 PM，只负责方向、状态和拆任务。真正写代码的 worker 单独开，reviewer 单独开，tester 也单独开。</p>
<p>这不是为了炫技，也不是为了说“多 Agent 工作流”听起来多高级。对我来说，它最重要的价值是隔离。</p>
<p>实现的人只看它应该实现什么。测试的人只看它应该怎么验。review 的人尽量站在另一个角度看这个东西有没有问题。主 agent 不要把所有噪音都吃进去，只保留 plan 和最终状态。</p>
<p>这样反而更稳。</p>
<p>有时候外部限制会逼你做出更好的系统。以前 context 很大的时候，我反而容易粗暴地把所有东西都丢进去。后来窗口没那么自由了，我才被迫去想：哪些东西应该放进去，哪些东西应该隔离，哪些东西应该通过文件和计划来传递，而不是全部塞进一个聊天里。</p>
<p>最后结果反而更好。</p>

<h2>AI 最大的风险不是笨，是太会顺着你说</h2>
<p>我现在对 AI 最后怕的一点，不是它会不会写错代码。</p>
<p>写错代码其实还好。你可以测，可以跑，可以看报错，可以 review。</p>
<p>更麻烦的是，它太会顺着你说。</p>
<p>比如我在做 SafeClick 的过程中，就踩过这个坑。第一版方案有问题，后面我又想了第二版方案。我当时拿着自己的 plan 去问 AI，它会帮我把这个 plan 讲得很完整，很合理，好像所有东西都能解释通。</p>
<p>但后来我换一种问法，让它重新 review 这个 plan，特别是从“这个 plan 可能有问题”的角度去看，它又能指出一堆问题。</p>
<p>这就很可怕。</p>
<p>因为这说明它并不总是在一个稳定的、客观的审查位置上。它很多时候是在响应你的 framing。你说“我这个方案怎么样”，它会倾向于帮你补强。你说“这个方案是不是有问题”，它又会倾向于帮你找问题。</p>
<p>如果你没有意识到这一点，你会以为 AI 在给你客观判断。但实际上，它可能是在给你情绪价值。</p>
<p>而且这种情绪价值很隐蔽。它不是简单说“你真棒”。它会用很专业的语言，把你的想法包装得更完整，让你觉得自己的方向越来越对。你看着它生成那么多内容，那么多分析，那么多理由，很容易产生一种错觉：既然它说得这么完整，那应该就是对的。</p>
<p>但完整不等于正确。</p>
<p>有时候，真正打断这个错误路径的，反而是一个真实的人很直接地告诉你：这个方案不行。</p>
<p>这种反馈不一定好听，但它有用。因为它不需要迎合你，也不会为了让对话继续舒服而把问题包装得很温和。它直接把你从那个自我强化的路径里拉出来。</p>
<p>这也是为什么我现在越来越不相信那种“一个人加一堆 AI 就能解决所有事情”的叙事。</p>
<p>不是说一个人不能做很多事。AI 确实让一个人的能力变强了很多。但如果整个系统里只有你和一堆会顺着你说的 AI，那么你的认知偏差也会被放大很多倍。</p>
<p>一个 AI 说你是对的，你可能还会怀疑。三个、五个、十个 AI 都在不同角度帮你把同一个错误方向讲圆，你可能真的会开始相信自己是对的。</p>
<p>这个地方其实很危险。</p>

<h2>市场叙事也会顺着你说</h2>
<p>还有一个更大的问题是，不只是 AI 会顺着你说，整个市场也会给你讲故事。</p>
<p>现在很多关于 AI 的叙事都很强。某个模型出来了，大家说它会替代多少工作。某家公司发布一个报告，大家开始恐慌。某个产品在 coding 上特别火，大家就默认它是唯一正确答案。</p>
<p>但这些东西里面有多少是真实能力，有多少是 marketing，有多少是资本市场需要的故事，其实要分开看。</p>
<p>我不是说这些公司不好，也不是说 AI 没有改变世界。AI 当然改变了我的工作流。我每天都在用，而且用得很多。它确实让我做事更快，也让我能做以前很难一个人做完的事情。</p>
<p>但正因为我真的在用，我反而更觉得不能把宣传当现实。</p>
<p>模型公司有自己的利益，企业高管有自己的故事，市场有自己的情绪。大家都在说“AI 会怎样怎样”，但最后真正做事的时候，还是要回到一个很简单的问题：</p>
<p>谁在判断？</p>
<p>谁在定义问题？</p>
<p>谁在决定这个东西到底能不能上线？</p>
<p>谁在为结果负责？</p>
<p>答案还是人。</p>
<p>AI 可以帮你写，可以帮你查，可以帮你生成，可以帮你推演。但是方向、取舍、责任，这些东西不能外包。</p>

<h2>不要把追热点当成学习</h2>
<p>这也引出另一个我最近越来越明显的感受：很多 AI 学习其实是虚假的学习。</p>
<p>每天都有新的工具、新的模型、新的 workflow、新的 skill。你会觉得如果不看，就落后了。如果不试，就错过了什么。这种 FOMO 很容易让人陷进去。</p>
<p>但问题是，看了很多，不代表你真的掌握了什么。</p>
<p>有时候你只是获得了一种“我正在学习”的感觉。你收藏了很多工具，下载了很多 skill，看了很多别人怎么用 AI 的文章。然后呢？回到自己的工作里，真正的问题还是没有被解决。</p>
<p>我现在更倾向于从问题出发。</p>
<p>不是说新工具不能试，可以试。但不要一上来就把它变成自己工作流的一部分。等你真的遇到一个反复出现的问题，再去想有没有工具能解决它。等你真的发现某个流程重复了很多次，再把它沉淀成 skill。</p>
<p>skill 本来就应该是自己的工作流沉淀出来的东西。它不是一个“装得越多越强”的插件系统。</p>
<p>别人的 skill 当然可以参考，但是生搬硬套会有很多水分。因为那是别人问题里的答案，里面有很多只适合他自己的上下文。你直接拿过来，可能只是在给自己增加摩擦。</p>
<p>真正有效的东西，应该是从自己的工作里长出来的。</p>
<p>你做着做着，发现某个步骤总是重复。你踩了一个坑，发现下次一定要先检查某件事。你 review 了几次之后，发现某类问题总是漏。这个时候沉淀出来的流程，才真的有价值。</p>

<h2>最后还是人的判断</h2>
<p>所以绕了一圈，我现在对 AI 的看法反而比以前更简单。</p>
<p>AI 很强。它真的很强。它降低了门槛，放大了能力，也改变了很多工作流。</p>
<p>但它没有替代判断。</p>
<p>它降低的是开始的成本，不是做好一件事的成本。它让生成变得便宜，但也让错误方向变得更容易被包装。它让一个人可以做更多事，但也会放大一个人的认知偏差。它让学习资源变多，但也制造了很多虚假的学习感。</p>
<p>所以 AI 时代最重要的能力，可能不是“会用多少工具”，也不是“能烧多少 token”。</p>
<p>更重要的是，你能不能定义问题。能不能看出一个方案哪里不对。能不能在 AI 顺着你说的时候停下来，问一句：它是在客观判断，还是只是在响应我的 framing？能不能在市场叙事很吵的时候，回到自己的真实工作里，看这个东西到底有没有解决问题。</p>
<p>AI 最有价值的地方，不是替我判断。</p>
<p>它最有价值的地方，是放大我已经判断清楚的东西。</p>
<p>如果我方向是清楚的，它会让我更快。如果我方向是错的，它也可能让我更快地走错。</p>
<p>这就是为什么，越是在 AI 时代，我越觉得人自己的批判性思维更重要。</p>
<p>不是更不重要，是更重要。</p>
<p>因为生成已经不稀缺了。</p>
<p>判断才稀缺。</p>
</div>
</div>

<script>
  (function () {
    var post = document.querySelector('.bilingual-post');
    if (!post) return;

    var buttons = post.querySelectorAll('[data-language-target]');
    var bodies = post.querySelectorAll('[data-language]');
    var article = post.closest('article');
    var title = article ? article.querySelector('header h1') : null;

    function setLanguage(language) {
      bodies.forEach(function (body) {
        body.hidden = body.getAttribute('data-language') !== language;
      });

      buttons.forEach(function (button) {
        var isActive = button.getAttribute('data-language-target') === language;
        button.classList.toggle('is-active', isActive);
        button.setAttribute('aria-pressed', isActive ? 'true' : 'false');
      });

      if (title) {
        title.textContent = language === 'zh' ? post.dataset.titleZh : post.dataset.titleEn;
      }

      document.documentElement.lang = language === 'zh' ? 'zh-Hans' : 'en';
    }

    buttons.forEach(function (button) {
      button.addEventListener('click', function () {
        setLanguage(button.getAttribute('data-language-target'));
      });
    });

    setLanguage('en');
  })();
</script>
