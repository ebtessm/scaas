# SCaaS: Software Components as a Service
# خدمة المكوّنات البرمجية كخدمة سحابية

> **Status / الحالة:** research idea and starting point. No working cloud service or code yet. Not an official government project.
> فكرة بحثية ونقطة بداية. لا توجد خدمة سحابية عاملة ولا كود تشغيلي حتى الآن. وليس مشروعًا حكوميًا رسميًا.

![SCaaS diagram](scaas-diagram.svg)

## الفكرة (عربي)

SCaaS طبقة خدمة سحابية جديدة تعرض **المكوّنات البرمجية كخدمة** فوق طبقات IaaS و PaaS و SaaS، لزيادة إعادة استخدام البرمجيات وتلبية الطلب المتزايد على البرمجيات.

من الرسم:

- **الإضافة (Add):** كود جديد يمر على *Code Indexer* الذي يفهرسه بطريقتين: فهرسة بالمفهوم (Concept Indexing) وفهرسة بالتوقيع (Signature Indexing)، ثم يُخزَّن في مخزن المكوّنات (SW Components).
- **الاسترجاع (Retrieve):** محرك بحث يختار تقنية البحث (كلمات مفتاحية، قائمة على المعرفة، بالأوجه Facet، دلالي Semantic، خوارزميات جينية)، ثم يتحقق من صلاحية المكوّن (Component Qualify)، ثم إعادة الاستخدام: Black Box أو White Box أو Glass Box.

## الربط بفكرة الحوسبة السحابية الوطنية

الفكرة المقترحة أن تكون SCaaS قلب منصة بحثية وتطويرية على حوسبة سحابية وطنية، تمهيدًا لتوطين تطبيقات الذكاء الاصطناعي وتصديرها. الخدمات المقترحة (أفكار للنقاش، وليست قائمة بما هو موجود):

1. بريد إلكتروني وطني.
2. تطبيقات ذكاء اصطناعي تعمل على السحابة الوطنية.
3. ألعاب إلكترونية بحساب موحد وخدمة السحابة.
4. بوابة إعلام وصحافة إلكترونية على السحابة الوطنية.
5. استكمال ربط أجهزة الدولة بخدمات الحوسبة السحابية.
6. منصة بحثية توليدية على غرار GitHub، لكن على السحابة الوطنية، مبنية على SCaaS.

التطبيق المرجعي الأول: [منصة السلامة على الطرق ونقل المواد الخطرة](https://github.com/ebtessm/egypt-road-safety-platform) ([عرض تجريبي](https://ebtessm.github.io/egypt-road-safety-platform/)). كل مكوّن فيها (تقييم المخاطر، التنبيهات) يمكن أن يُنشر كمكوّن قابل لإعادة الاستخدام عبر SCaaS.

## English summary

SCaaS adds a "software components" service layer on top of IaaS, PaaS and SaaS to raise software reuse. New code goes through a code indexer (concept and signature indexing) into a component store. Retrieval uses a search engine that picks a technique (keyword, knowledge, facet, semantic, genetic algorithm), qualifies the component, then supports black-box, white-box or glass-box reuse.

The proposal here is to build a national-cloud research and development platform around SCaaS, to localize and export AI applications. First reference application: the [road safety platform](https://github.com/ebtessm/egypt-road-safety-platform).

## مبدأ التكامل داخل SCaaS / The integration principle

الخدمات المقترحة لا تُبنى كل واحدة منفصلة، بل تتكامل: مكوّن يُبنى مرة واحدة ويُفهرس في SCaaS، ثم تعيد استخدامه أكثر من خدمة. أمثلة على مكوّنات مشتركة مقترحة: الحسابات والصلاحيات، التنبيهات والإشعارات، التقارير وتحليل البيانات، وخدمات الذكاء الاصطناعي. الخدمتان التجريبيتان أدناه (السلامة على الطرق، وكويزورا) مثالان على ذلك: تنبيهات المخاطر في الأولى وتنبيهات المتابعة والتقارير في الثانية يمكن أن يشتركا في مكوّن واحد.

هذا مبدأ تصميم مقترح. لم يُنفَّذ أي مكوّن مشترك بعد، والمشروعان الحاليان منفصلان تمامًا.

**English:** Services are not built in isolation. A component is built once, indexed in SCaaS and reused by several services (for example accounts and permissions, alerts and notifications, reporting and analytics, AI services). The two pilot services below are examples. This is a proposed design principle: no shared component exists yet and the two current projects are fully separate.

## خدمة تجريبية مقترحة: منصة السلامة على الطرق ونقل المواد الخطرة / Pilot service: road safety platform

**الفكرة:** [منصة السلامة على الطرق ونقل المواد الخطرة](https://github.com/ebtessm/egypt-road-safety-platform) ([عرض تجريبي](https://ebtessm.github.io/egypt-road-safety-platform/)) هي أول فكرة للمشروع، وجاءت بعد حادث الوراق. تُقترح كخدمة تجريبية ثانية على السحابة الوطنية، ويمكن نشر مكوناتها (تقييم المخاطر، التنبيهات) كمكوّنات قابلة لإعادة الاستخدام عبر SCaaS.

**ما هو موجود فعلًا اليوم:**

- مستودع مفتوح المصدر فيه الرؤية والبنية ونموذج البيانات وخطة المراحل.
- نموذج أولي بسيط بلغة Python يحسب درجة الخطر ويولّد تنبيهات، مع اختبارات وبيانات تجريبية مصنوعة (ليست بيانات حقيقية).
- صفحة عرض تجريبي على GitHub Pages.

**ما هو مقترح ولم يُنفَّذ بعد:**

- ربط الجهات المعنية (المرور، الإسعاف، الحماية المدنية، شركات النقل، الجهات الرقابية) في منصة واحدة.
- تتبع لحظي حقيقي للناقلات عبر أجهزة GPS.
- نشر مكوّناتها عبر SCaaS واستضافتها على سحابة وطنية.
- مراجعة الأوزان والحدود من خبراء السلامة والجهات المختصة قبل أي استخدام فعلي.

**ملاحظة صريحة:** لا يوجد تتبع حقيقي ولا ربط بأي جهة، والنموذج الأولي لإثبات الفكرة فقط، وليس مشروعًا حكوميًا رسميًا.

**English:** The [road safety and hazardous-materials transport platform](https://github.com/ebtessm/egypt-road-safety-platform) (first idea, prompted by the Warraq crash) is proposed as a second pilot service. *Exists today:* open-source repo with vision, architecture, data model and roadmap; a small Python risk-scoring and alert prototype with tests and synthetic sample data; a demo page. *Planned, not built:* linking the agencies on one platform, real-time GPS tracking, publishing its parts as SCaaS components, national-cloud hosting, expert review of the risk weights. *Honest status:* no real tracking and no agency integration yet; prototype for the idea only, not an official government project.

## كويزورا: خدمة تجريبية مقترحة ضمن SCaaS / Quizora as a pilot service

**الفكرة:** [تحدي كويزورا (Quizora)](https://ebtessm.github.io/quiz/) منصة اختبارات وتدريب تفاعلية، تُقترح كأول **خدمة تجريبية** يمكن أن تنبثق من السحابة الوطنية وSCaaS، بهدف حماية أبنائنا وتنمية العقول والمهارات التعليمية.

**ما تفعله كويزورا فعلًا اليوم (نموذج أولي يعمل على الإنترنت):**

- موقع اختبارات تفاعلي مجاني على GitHub Pages مع قاعدة بيانات Supabase.
- أنواع أسئلة متعددة: اختيار من متعدد، صح/خطأ، أكمل، توصيل، ترتيب، واكتشف الخطأ في الكود.
- حسابات للمدربين: رفع ملف (PDF أو Word أو نص) وتوليد أسئلة بخدمة ذكاء اصطناعي خارجية، ثم مشاركة رابط الاختبار ومتابعة النتائج. الأسئلة المولدة تحتاج مراجعة بشرية.
- تسجيل المشاركين بالاسم والبريد الإلكتروني قبل الاختبار.
- بنوك أسئلة جاهزة أُعدت للموقع، وليست مصدرًا رسميًا أو معتمدًا.

**ما هو مقترح ولم يُنفَّذ بعد:**

- نشر مكوّنات كويزورا (توليد الأسئلة، تصحيح الأنواع المختلفة، تقارير النتائج) كمكوّنات قابلة لإعادة الاستخدام عبر SCaaS.
- استضافتها على سحابة وطنية بدل الخدمات الخارجية الحالية.
- ضوابط حماية الأطفال: مراجعة المحتوى حسب العمر، بدون إعلانات أو تتبع، حد أدنى من البيانات الشخصية، وصلاحيات للمعلم وولي الأمر.
- مسارات تعلّم ومهارات وتقارير تقدّم للطالب.

**ملاحظة صريحة:** كويزورا اليوم لا تعمل على سحابة وطنية، ولم تُبنَ من مكوّنات SCaaS، وليس فيها ضوابط مخصصة لحماية الأطفال بعد. هذا القسم يعرض اتجاهًا مقترحًا وليس خدمة قائمة.

**English:** [Quizora](https://ebtessm.github.io/quiz/) is proposed as the first pilot service derived from the SCaaS / national cloud idea, to help protect children and build learning skills.

*Works today (live prototype):* a free interactive quiz site (GitHub Pages and Supabase); several question types; trainer accounts that upload a document and auto-generate questions with an external AI service (output needs human review); shareable quiz links and results; participant registration with name and email; question banks written for the site, not an official source.

*Planned, not built:* publishing Quizora's parts (question generation, grading, reports) as reusable SCaaS components; hosting on a national cloud; child-safety controls (age-appropriate content review, no ads or tracking, minimal data, teacher and parent controls); learning paths and progress reports.

*Honest status:* Quizora does not run on a national cloud, is not built from SCaaS components, and has no dedicated child-protection features yet. This section describes a proposed direction, not an existing service.

## What exists now / ما الموجود فعلًا

- The diagram and this description only. / الرسم والوصف فقط.
- See [ROADMAP.md](ROADMAP.md) for proposed next steps. / خطوات مقترحة في ملف الخطة.
- Quizora: a separate live quiz prototype, proposed as a pilot service (see section above). / كويزورا: نموذج أولي منفصل يعمل، ومقترح كخدمة تجريبية (انظر القسم أعلاه).

## Contributing

Open an issue to discuss ideas, or send a pull request. Experts in cloud computing, software reuse and public-sector IT are especially welcome.

## License

MIT, see [LICENSE](LICENSE). Copyright (c) 2026 Ebtessam Desouky and contributors.
