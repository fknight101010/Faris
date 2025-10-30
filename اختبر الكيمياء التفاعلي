<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اختبار كيمياء تفاعلي</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, rgba(52, 152, 219, 0.8), rgba(142, 68, 173, 0.8)), url('IMG_0433.jpeg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            width: 100%;
            max-width: 800px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }
        
        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
        }
        
        .page {
            display: none;
            padding: 30px;
        }
        
        .active {
            display: block;
        }
        
        .form-group {
            margin-bottom: 15px;
        }
        
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #2c3e50;
        }
        
        input, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        .btn {
            display: inline-block;
            background-color: #3498db;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 10px;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #2980b9;
        }
        
        .btn:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
        }
        
        .btn-container {
            text-align: center;
            margin-top: 20px;
        }
        
        .question-page {
            display: none;
        }
        
        .question-page.active {
            display: block;
        }
        
        .question-number {
            font-weight: bold;
            margin-bottom: 10px;
            color: #2c3e50;
            font-size: 20px;
        }
        
        .question-text {
            font-size: 22px;
            margin-bottom: 25px;
            color: #2c3e50;
            line-height: 1.5;
        }
        
        .options {
            margin-bottom: 30px;
        }
        
        .option {
            margin-bottom: 15px;
            padding: 15px;
            background-color: #f8f9fa;
            border: 2px solid #e9ecef;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 18px;
        }
        
        .option:hover {
            background-color: #e9ecef;
            transform: translateY(-2px);
        }
        
        .option.selected {
            background-color: #d4edda;
            border-color: #c3e6cb;
            color: #155724;
        }
        
        .option.correct {
            background-color: #d4edda;
            border-color: #c3e6cb;
            color: #155724;
        }
        
        .option.incorrect {
            background-color: #f8d7da;
            border-color: #f5c6cb;
            color: #721c24;
        }
        
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }
        
        .timer {
            text-align: center;
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #e74c3c;
        }
        
        .results {
            margin-top: 20px;
        }
        
        .result-item {
            margin-bottom: 15px;
            padding: 10px;
            border-radius: 5px;
        }
        
        .correct {
            background-color: #d4edda;
            border: 1px solid #c3e6cb;
        }
        
        .incorrect {
            background-color: #f8d7da;
            border: 1px solid #f5c6cb;
        }
        
        .progress-bar {
            height: 8px;
            background-color: #e9ecef;
            border-radius: 4px;
            margin-bottom: 20px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(135deg, #3498db, #8e44ad);
            border-radius: 4px;
            transition: width 0.5s ease;
        }
        
        .progress-text {
            text-align: center;
            margin-bottom: 10px;
            font-weight: bold;
            color: #2c3e50;
        }
        
        .feedback {
            text-align: center;
            margin-top: 15px;
            font-weight: bold;
            font-size: 18px;
            min-height: 30px;
        }
        
        .correct-feedback {
            color: #27ae60;
        }
        
        .incorrect-feedback {
            color: #e74c3c;
        }
        
        .audio-controls {
            text-align: center;
            margin: 10px 0;
        }
        
        .audio-btn {
            background-color: #2ecc71;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            margin: 0 5px;
        }
        
        .team-members {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #ddd;
        }
        
        .team-members h3 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .team-members p {
            color: #7f8c8d;
            font-size: 16px;
        }
        
        @media (max-width: 768px) {
            .question-text {
                font-size: 20px;
            }
            
            .option {
                font-size: 16px;
                padding: 12px;
            }
            
            .navigation {
                flex-direction: column;
                gap: 10px;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- الصفحة الأولى: معلومات الطالب -->
    <div class="container page active" id="page1">
        <h1>اختبار كيمياء تفاعلي</h1>
        <div class="form-group">
            <label for="studentName">الاسم:</label>
            <input type="text" id="studentName" placeholder="أدخل اسمك">
        </div>
        <div class="form-group">
            <label for="studentClass">الشعبة:</label>
            <select id="studentClass">
                <option value="">اختر شعبتك</option>
                <option value="1">شعبة 1</option>
                <option value="2">شعبة 2</option>
                <option value="3">شعبة 3</option>
                <option value="4">شعبة 4</option>
                <option value="5">شعبة 5</option>
                <option value="6">شعبة 6</option>
                <option value="7">شعبة 7</option>
            </select>
        </div>
        
        <div class="audio-controls">
            <p>تفعيل الأصوات:</p>
            <button class="audio-btn" id="enableSound">تشغيل الأصوات</button>
            <button class="audio-btn" id="disableSound">إيقاف الأصوات</button>
        </div>
        
        <div class="btn-container">
            <button class="btn" id="startTest">بدء الاختبار</button>
        </div>
        <p style="text-align: center; margin-top: 20px; font-weight: bold;">
            اختبار كيمياء الباب الثاني - 48 سؤال في 50 دقيقة
        </p>
    </div>

    <!-- الصفحة الثانية: الأسئلة (صفحات منفصلة لكل سؤال) -->
    <div class="container page" id="page2">
        <h1>اختبار كيمياء تفاعلي</h1>
        <div class="timer" id="timer">50:00</div>
        
        <div class="progress-text">السؤال <span id="currentQuestion">1</span> من <span id="totalQuestions">48</span></div>
        <div class="progress-bar">
            <div class="progress" id="progressBar" style="width: 2.08%;"></div>
        </div>
        
        <!-- صفحات الأسئلة المنفصلة -->
        <div id="questionPagesContainer">
            <!-- سيتم إضافة صفحات الأسئلة هنا عبر JavaScript -->
        </div>
        
        <div class="navigation">
            <button class="btn" id="prevBtn" style="display: none;">السابق</button>
            <button class="btn" id="nextBtn" disabled>التالي</button>
            <button class="btn" id="submitBtn" style="display: none;">إنهاء الاختبار</button>
        </div>
    </div>

    <!-- الصفحة الثالثة: النتائج -->
    <div class="container page" id="page3">
        <h1>نتائج اختبار الكيمياء</h1>
        <div id="studentInfo"></div>
        <div id="scoreContainer" style="text-align: center; margin: 20px 0;">
            <h2 id="scoreText"></h2>
            <h3 id="timeTaken"></h3>
        </div>
        <div id="resultsContainer" class="results">
            <!-- سيتم عرض النتائج هنا -->
        </div>
        
        <div class="team-members">
            <h3>فريق العمل:</h3>
            <p>فارس المبرزي، بتال الوادعي، علي الأحمري، أحمد ربيعة، فيصل العبيد، ياسر الأحمري، عاصم الغامدي</p>
        </div>
        
        <div class="btn-container">
            <button class="btn" id="restartTest">إعادة الاختبار</button>
        </div>
    </div>

    <script>
        // تعريف الأسئلة والإجابات المدمجة
        const questions = [
            // الأسئلة الأصلية من الملف (28 سؤال)
            {
                question: "الهدف من استخدام الطريقة العلمية:",
                options: ["حل المشكلات", "اكتساب المعرفة", "جمع المعلومات"],
                correctAnswer: 0
            },
            {
                question: "أحد الملاحظات التالية تصنف من البيانات النوعية:",
                options: ["اللون", "العرض", "الوزن"],
                correctAnswer: 0
            },
            {
                question: "كل فرضية يتم افتراضها تكون:",
                options: ["مؤقتة", "صحيحة", "خاطئة"],
                correctAnswer: 0
            },
            {
                question: "عندما تدعم الفرضية بالتجارب تتحول إلى:",
                options: ["قانون علمي", "النظرية", "استراتيجية"],
                correctAnswer: 1
            },
            {
                question: "تفسير مؤقت لظاهرة ما أو حدث تمت ملاحظته:",
                options: ["القانون العلمي", "النظرية", "الفرضية"],
                correctAnswer: 2
            },
            {
                question: "المتغير الذي يخطط لتغيره في التجربة:",
                options: ["المتغير المستقل", "المتغير التابع", "الضابط"],
                correctAnswer: 0
            },
            {
                question: "معيار يستعمل للمقارنة في التجربة:",
                options: ["المتغير المستقل", "المتغير التابع", "الضابط"],
                correctAnswer: 2
            },
            {
                question: "حكم على المعلومات التي يتم الحصول عليها:",
                options: ["الاستنتاج", "التجربة", "الملاحظة"],
                correctAnswer: 0
            },
            {
                question: "مجموعة من المشاهدات المضبوطة التي تختبر الفرضية:",
                options: ["الملاحظة", "التجربة", "النتيجة"],
                correctAnswer: 1
            },
            {
                question: "يعتبر الشمع مثال على مادة:",
                options: ["غازية", "صلبة", "سائلة"],
                correctAnswer: 1
            },
            {
                question: "كلمة تشير إلى الحالة الغازية لمادة توجد بشكل صلب أو سائل في درجات الحرارة العادية:",
                options: ["الاحتراق", "البخار", "الغاز"],
                correctAnswer: 1
            },
            {
                question: "خاصية يمكن ملاحظتها دون تغير في تركيب العينة:",
                options: ["الخاصية الفيزيائية", "الخاصية الكيميائية", "الخاصية البلازمية"],
                correctAnswer: 0
            },
            {
                question: "من الأمثلة على الخواص الفيزيائية المميزة:",
                options: ["الطول", "الكثافة", "الحجم"],
                correctAnswer: 1
            },
            {
                question: "يعتبر تكون الصدا:",
                options: ["خاصية كيميائية", "خاصية فيزيائية", "خاصية غير مميزة"],
                correctAnswer: 0
            },
            {
                question: "تفاعلت عينة مقدارها 10 جرام من المغنيسيوم لتكوين 16.6 من أكسيد المغنيسيوم، فأن كمية الأكسجين:",
                options: ["6.6 جم", "10 جم", "26.6 جم"],
                correctAnswer: 0
            },
            {
                question: "يعتبر تعفن الخبز مثال على:",
                options: ["تغير فيزيائي", "تغير كيميائي"],
                correctAnswer: 1
            },
            {
                question: "تعتبر حشوة الاسنان:",
                options: ["مركب", "مخلوط"],
                correctAnswer: 1
            },
            {
                question: "عملية تتبخر فيها المواد الصلبة دون أن تنصهر:",
                options: ["الترشيح", "الكروماتوغرافيا"],
                correctAnswer: 1
            },
            {
                question: "طريقة للفصل تؤدي للحصول على مادة ثقيلة من محلولها:",
                options: ["التبلور", "التقطير"],
                correctAnswer: 0
            },
            {
                question: "اسطوانة الغوص مصنوعة من مزيج من المعادن تعتبر محلول من نوع:",
                options: ["صلب - صلب", "سائل - سائل"],
                correctAnswer: 0
            },
            {
                question: "الأعمدة الرأسية في الجدول الدوري:",
                options: ["المجموعات", "الدورات"],
                correctAnswer: 0
            },
            {
                question: "تسمى الصفوف الأفقية في الجدول الدوري:",
                options: ["العائلات", "المجموعات"],
                correctAnswer: 1
            },
            {
                question: "في تجربة التحليل الكهربائي للماء تكون:",
                options: ["كمية الهيدروجين ضعف الأكسجين", "كمية الأكسجين ضعف الهيدروجين"],
                correctAnswer: 0
            },
            {
                question: "يتفاعل 1 جم من الهيدروجين مع 19 جم فلور، فالنسبة المئوية بالكتلة للهيدروجين في المركب:",
                options: ["95%", "5%"],
                correctAnswer: 1
            },
            {
                question: "عينة من مركب مجهول كتلتها 100 جم تحتوي على 20 جم هيدروجين، فالنسبة المئوية للهيدروجين:",
                options: ["10%", "20%"],
                correctAnswer: 1
            },
            {
                question: "القانون المستخدم للمقارنة بين CO و CO₂:",
                options: ["النسب الثابتة", "حفظ الكتلة"],
                correctAnswer: 0
            },
            {
                question: "النحاس موصل جيد للكهرباء:",
                options: ["خاصية كيميائية", "خاصية فيزيائية"],
                correctAnswer: 1
            },
            {
                question: "أول من صمم جدول دورياً للعناصر هو...... و ذلك حسب الكتل الذرية لها:",
                options: ["بيتري", "مندليف", "جواهام"],
                correctAnswer: 1
            },
            
            // الأسئلة الإضافية (20 سؤال)
            {
                question: "ما الفرق الرئيسي بين الماء النقي وماء البحر?",
                options: [
                    "الماء النقي موصل للكهرباء بينما ماء البحر ليس كذلك",
                    "الماء النقي مخلوط متجانس بينما ماء البحر مادة نقية",
                    "الماء النقي مادة نقية بينما ماء البحر مخلوط من الماء والأملاح"
                ],
                correctAnswer: 2
            },
            {
                question: "أي من الآتي يصف حالات المادة الثلاث الرئيسية?",
                options: [
                    "الصلبة، السائلة، البلازما",
                    "الصلبة، السائلة، الغازية",
                    "المعدنية، العضوية، الحيوية"
                ],
                correctAnswer: 1
            },
            {
                question: "ما أوجه المقارنة الأساسية بين الحالة الصلبة والسائلة للمادة?",
                options: [
                    "الجزيئات في الحالة الصلبة أكثر حرية في الحركة",
                    "للمادة في الحالة الصلبة شكل وحجم ثابتان، بينما في الحالة السائلة حجم ثابت وشكل غير ثابت",
                    "الجزيئات في الحالة السائلة مترابطة بشدة كما في الصلبة"
                ],
                correctAnswer: 1
            },
            {
                question: "ما الفرق الأساسي بين الغاز والبخار?",
                options: [
                    "البخار هو غاز يمكن رؤيته بالعين بينما الغاز لا يمكن رؤيته",
                    "الغاز يكون دائماً في درجة حرارة الغرفة بينما البخار يكون ساخناً",
                    "البخار هو الحالة الغازية لمادة تكون سائلة أو صلبة في درجة حرارة الغرفة"
                ],
                correctAnswer: 2
            },
            {
                question: "ما تعريف الخواص الفيزيائية?",
                options: [
                    "هي الخواص التي تصف قابلية المادة للتفاعل مع غيرها",
                    "هي الخواص التي تصف سلوك المادة عند تعرضها للهب",
                    "هي الخواص التي يمكن ملاحظتها أو قياسها دون تغيير التركيب الداخلي للمادة"
                ],
                correctAnswer: 2
            },
            {
                question: "أي من الآتي يمثل أفضل مقارنة بين الخواص الفيزيائية المميزة وغير المميزة?",
                options: [
                    "الخواص المميزة تعتمد على الكمية بينما غير المميزة لا تعتمد",
                    "الخواص المميزة تساعد في تحديد هوية المادة (مثل الكثافة) بينما غير المميزة (مثل الكتلة) لا تساعد",
                    "الخواص غير المميزة هي خواص كيميائية بينما المميزة هي فيزيائية"
                ],
                correctAnswer: 1
            },
            {
                question: "ما تعريف الخواص الكيميائية?",
                options: [
                    "هي خواص لا تتغير مع تغير كمية المادة",
                    "هي الخواص التي تصف مظهر المادة",
                    "هي الخواص التي تصف كيفية تفاعل المادة لتكوين مواد جديدة"
                ],
                correctAnswer: 2
            },
            {
                question: "أي من الأمثلة التالية يعد دليلاً على تغير كيميائي?",
                options: [
                    "ذوبان السكر في الماء",
                    "تكثف بخار الماء على زجاج نافذة",
                    "تغير لون ورقة الشجر في الخريف"
                ],
                correctAnswer: 2
            },
            {
                question: "أي من العوامل الخارجية التالية يؤثر بشكل مباشر على تغير حالات المادة?",
                options: [
                    "اللون والطعم",
                    "درجة الحرارة والضغط",
                    "الشكل والحجم"
                ],
                correctAnswer: 1
            },
            {
                question: "إذا تفاعل 10 غرامات من الهيدروجين مع 80 غراماً من الأكسجين، فما كتلة الماء الناتج وفقاً لقانون حفظ الكتلة?",
                options: [
                    "70 غراماً",
                    "80 غراماً",
                    "90 غراماً"
                ],
                correctAnswer: 2
            },
            {
                question: "أي من الآتي يعد من أدلة حدوث التفاعل الكيميائي?",
                options: [
                    "تغير في حالة المادة من سائلة إلى صلبة فقط",
                    "تغير في اللون أو تكون راسب",
                    "زيادة كتلة المواد المتفاعلة"
                ],
                correctAnswer: 1
            },
            {
                question: "أي من الأمثلة التالية يصف تغيراً فيزيائياً?",
                options: [
                    "حرق قطعة من الورق",
                    "صدأ الحديد",
                    "تقطيع التفاحة إلى شرائح"
                ],
                correctAnswer: 2
            },
            {
                question: "ما أفضل وصف للمخاليط?",
                options: [
                    "مواد نقية تتكون من نوع واحد من الذرات",
                    "مزيج من مادتين أو أكثر تحتفظ كل منهما بخواصها",
                    "مواد تنتج عن اتحاد عنصرين بنسب ثابتة"
                ],
                correctAnswer: 1
            },
            {
                question: "ما الفرق الرئيسي بين المخلوط المتجانس وغير المتجانس?",
                options: [
                    "المتجانس لا يمكن فصله بينما غير المتجانس يمكن فصله",
                    "المتجانس له تركيب موحد في جميع أجزائه، بينما غير المتجانس لا",
                    "غير المتجانس مادة نقية بينما المتجانس مخلوط"
                ],
                correctAnswer: 1
            },
            {
                question: "أي من الطرق التالية ستكون الأفضل لفصل مخلوط من الرمل والملح?",
                options: [
                    "التسخين المباشر حتى الاحتراق",
                    "الذوبان في الماء ثم الترشيح ثم التبخير",
                    "التبريد حتى التجمد"
                ],
                correctAnswer: 1
            },
            {
                question: "أي من الآتي يعد تصنيفاً صحيحاً لأنواع المحاليل?",
                options: [
                    "صلبة، سائلة، غازية",
                    "مشبعة، غير مشبعة، فوق مشبعة",
                    "حامضية، قاعدية، متعادلة"
                ],
                correctAnswer: 1
            },
            {
                question: "كيف يتم ترتيب العناصر في الجدول الدوري الحديث?",
                options: [
                    "حسب الكتلة الذرية تنازلياً",
                    "حسب العدد الذري (عدد البروتونات) تصاعدياً",
                    "حسب تاريخ اكتشافها"
                ],
                correctAnswer: 1
            },
            {
                question: "ما الذي ينص عليه قانون النسب المتضاعفة (دالتون)?",
                options: [
                    "أن كتلة المادة لا تفنى ولا تستحدث في التفاعل الكيميائي",
                    "عندما يتحد عنصران لتكوين أكثر من مركب، فإن النسبة الكتلية لأحد العناصر التي تتحد مع كتلة ثابتة من الآخر تكون على شكل أعداد صحيحة بسيطة",
                    "أن العناصر تتحد بنسب وزنية ثابتة لتكوين مركب محدد"
                ],
                correctAnswer: 1
            },
            {
                question: "ما الفرق الأساسي بين العنصر والمركب?",
                options: [
                    "العنصر مادة نقية لا يمكن تحليلها إلى مواد أبسط، بينما المركب يتكون من عنصرين أو أكثر متحدين كيميائياً",
                    "العنصر مخلوط متجانس بينما المركب مخلوط غير المتجانس",
                    "العنصر موجود في الطبيعة فقط، بينما المركب يصنعه الإنسان فقط"
                ],
                correctAnswer: 0
            },
            {
                question: "ما الاسم العلمي والصيغة الكيميائية لملح الطعام?",
                options: [
                    "كربونات الصوديوم (Na₂CO₃)",
                    "كلوريد الصوديوم (NaCl)",
                    "كبريتات الصوديوم (Na₂SO₄)"
                ],
                correctAnswer: 1
            }
        ];

        // متغيرات التطبيق
        let currentPage = 1;
        let currentQuestionIndex = 0;
        let studentAnswers = new Array(questions.length).fill(null);
        let timerInterval;
        let timeLeft = 50 * 60; // 50 دقيقة بالثواني
        let startTime;
        let endTime;
        let soundEnabled = true;

        // عناصر DOM
        const pages = document.querySelectorAll('.page');
        const startTestBtn = document.getElementById('startTest');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const submitBtn = document.getElementById('submitBtn');
        const restartTestBtn = document.getElementById('restartTest');
        const timerElement = document.getElementById('timer');
        const questionPagesContainer = document.getElementById('questionPagesContainer');
        const studentInfoElement = document.getElementById('studentInfo');
        const scoreTextElement = document.getElementById('scoreText');
        const timeTakenElement = document.getElementById('timeTaken');
        const resultsContainer = document.getElementById('resultsContainer');
        const currentQuestionElement = document.getElementById('currentQuestion');
        const totalQuestionsElement = document.getElementById('totalQuestions');
        const progressBar = document.getElementById('progressBar');
        const enableSoundBtn = document.getElementById('enableSound');
        const disableSoundBtn = document.getElementById('disableSound');

        // تهيئة التطبيق
        function init() {
            // إضافة المستمعين للأحداث
            startTestBtn.addEventListener('click', startTest);
            prevBtn.addEventListener('click', goToPrevQuestion);
            nextBtn.addEventListener('click', goToNextQuestion);
            submitBtn.addEventListener('click', submitTest);
            restartTestBtn.addEventListener('click', restartTest);
            enableSoundBtn.addEventListener('click', () => enableSound(true));
            disableSoundBtn.addEventListener('click', () => enableSound(false));
            
            // إنشاء صفحات الأسئلة المنفصلة
            createQuestionPages();
            
            // تحديث عدد الأسئلة الإجمالي
            totalQuestionsElement.textContent = questions.length;
        }

        // تفعيل/تعطيل الصوت
        function enableSound(enabled) {
            soundEnabled = enabled;
            if (enabled) {
                enableSoundBtn.style.backgroundColor = '#2ecc71';
                disableSoundBtn.style.backgroundColor = '#95a5a6';
            } else {
                enableSoundBtn.style.backgroundColor = '#95a5a6';
                disableSoundBtn.style.backgroundColor = '#e74c3c';
            }
        }

        // تشغيل صوت الإجابة الصحيحة
        function playCorrectSound() {
            if (!soundEnabled) return;
            
            try {
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
                
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                
                oscillator.frequency.value = 800;
                oscillator.type = 'sine';
                
                gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 1);
                
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 1);
            } catch (e) {
                console.log('لا يمكن تشغيل الصوت في هذا المتصفح');
            }
        }

        // تشغيل صوت الإجابة الخاطئة
        function playIncorrectSound() {
            if (!soundEnabled) return;
            
            try {
                const audioContext = new (window.AudioContext || window.webkitAudioContext)();
                const oscillator = audioContext.createOscillator();
                const gainNode = audioContext.createGain();
                
                oscillator.connect(gainNode);
                gainNode.connect(audioContext.destination);
                
                oscillator.frequency.value = 400;
                oscillator.type = 'sawtooth';
                
                gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
                gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 1);
                
                oscillator.start(audioContext.currentTime);
                oscillator.stop(audioContext.currentTime + 1);
            } catch (e) {
                console.log('لا يمكن تشغيل الصوت في هذا المتصفح');
            }
        }

        // إنشاء صفحات الأسئلة المنفصلة
        function createQuestionPages() {
            questions.forEach((q, index) => {
                const questionPage = document.createElement('div');
                questionPage.className = 'question-page';
                questionPage.id = `question-page-${index}`;
                
                const questionNumber = document.createElement('div');
                questionNumber.className = 'question-number';
                questionNumber.textContent = `سؤال ${index + 1}`;
                
                const questionText = document.createElement('div');
                questionText.className = 'question-text';
                questionText.textContent = q.question;
                
                const optionsContainer = document.createElement('div');
                optionsContainer.className = 'options';
                
                q.options.forEach((option, optIndex) => {
                    const optionElement = document.createElement('div');
                    optionElement.className = 'option';
                    optionElement.setAttribute('data-value', optIndex);
                    optionElement.textContent = option;
                    
                    optionElement.addEventListener('click', () => {
                        handleOptionClick(index, optIndex, optionElement);
                    });
                    
                    optionsContainer.appendChild(optionElement);
                });
                
                const feedback = document.createElement('div');
                feedback.className = 'feedback';
                feedback.id = `feedback-${index}`;
                
                questionPage.appendChild(questionNumber);
                questionPage.appendChild(questionText);
                questionPage.appendChild(optionsContainer);
                questionPage.appendChild(feedback);
                
                questionPagesContainer.appendChild(questionPage);
            });
            
            // إظهار السؤال الأول
            showQuestion(0);
        }

        // التعامل مع النقر على خيار الإجابة
        function handleOptionClick(questionIndex, optionIndex, optionElement) {
            // حفظ إجابة الطالب
            studentAnswers[questionIndex] = optionIndex;
            
            // إزالة التحديد من جميع الخيارات في هذا السؤال
            const allOptions = optionElement.parentElement.querySelectorAll('.option');
            allOptions.forEach(opt => {
                opt.classList.remove('selected');
            });
            
            // تحديد الخيار المختار
            optionElement.classList.add('selected');
            
            // تفعيل زر التالي
            nextBtn.disabled = false;
            
            // التحقق من الإجابة وعرض التغذية الراجعة
            checkAnswer(questionIndex, optionIndex);
        }

        // التحقق من الإجابة وعرض التغذية الراجعة
        function checkAnswer(questionIndex, selectedAnswer) {
            const question = questions[questionIndex];
            const feedbackElement = document.getElementById(`feedback-${questionIndex}`);
            const allOptions = document.querySelectorAll(`#question-page-${questionIndex} .option`);
            
            if (selectedAnswer === question.correctAnswer) {
                // الإجابة صحيحة
                feedbackElement.textContent = "إجابة صحيحة! ✓";
                feedbackElement.className = "feedback correct-feedback";
                playCorrectSound();
                
                // تلوين الخيار الصحيح
                allOptions.forEach(option => {
                    if (parseInt(option.getAttribute('data-value')) === question.correctAnswer) {
                        option.classList.add('correct');
                    }
                });
            } else {
                // الإجابة خاطئة
                feedbackElement.textContent = "إجابة خاطئة! ✗";
                feedbackElement.className = "feedback incorrect-feedback";
                playIncorrectSound();
                
                // تلوين الخيارات
                allOptions.forEach(option => {
                    const optionValue = parseInt(option.getAttribute('data-value'));
                    if (optionValue === question.correctAnswer) {
                        option.classList.add('correct');
                    } else if (optionValue === selectedAnswer) {
                        option.classList.add('incorrect');
                    }
                });
            }
        }

        // إظهار سؤال محدد
        function showQuestion(questionIndex) {
            // إخفاء جميع صفحات الأسئلة
            document.querySelectorAll('.question-page').forEach(page => {
                page.classList.remove('active');
            });
            
            // إظهار السؤال المطلوب
            document.getElementById(`question-page-${questionIndex}`).classList.add('active');
            
            // تحديث السؤال الحالي
            currentQuestionIndex = questionIndex;
            currentQuestionElement.textContent = currentQuestionIndex + 1;
            
            // تحديث شريط التقدم
            updateProgressBar();
            
            // تحديث حالة أزرار التنقل
            updateNavigationButtons();
            
            // تعطيل زر التالي حتى يتم اختيار إجابة
            nextBtn.disabled = studentAnswers[currentQuestionIndex] === null;
        }

        // تحديث شريط التقدم
        function updateProgressBar() {
            const progressPercentage = ((currentQuestionIndex + 1) / questions.length) * 100;
            progressBar.style.width = `${progressPercentage}%`;
        }

        // الانتقال إلى السؤال السابق
        function goToPrevQuestion() {
            if (currentQuestionIndex > 0) {
                showQuestion(currentQuestionIndex - 1);
            }
        }

        // الانتقال إلى السؤال التالي
        function goToNextQuestion() {
            if (currentQuestionIndex < questions.length - 1) {
                showQuestion(currentQuestionIndex + 1);
            }
        }

        // تحديث أزرار التنقل
        function updateNavigationButtons() {
            // تحديث أزرار السابق
            prevBtn.style.display = currentQuestionIndex === 0 ? 'none' : 'inline-block';
            
            // تحديث أزرار التالي
            nextBtn.style.display = currentQuestionIndex === questions.length - 1 ? 'none' : 'inline-block';
            
            // تحديث زر الإرسال
            submitBtn.style.display = currentQuestionIndex === questions.length - 1 ? 'inline-block' : 'none';
        }

        // بدء الاختبار
        function startTest() {
            const studentName = document.getElementById('studentName').value;
            const studentClass = document.getElementById('studentClass').value;
            
            if (!studentName || !studentClass) {
                alert('يرجى إدخال الاسم واختيار الشعبة');
                return;
            }
            
            // تسجيل وقت بدء الاختبار
            startTime = new Date();
            
            // الانتقال إلى صفحة الأسئلة
            showPage(2);
            
            // بدء المؤقت
            startTimer();
        }

        // بدء المؤقت
        function startTimer() {
            updateTimerDisplay();
            
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimerDisplay();
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    submitTest();
                }
            }, 1000);
        }

        // تحديث عرض المؤقت
        function updateTimerDisplay() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            timerElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            
            // تغيير اللون عندما يقل الوقت عن 10 دقائق
            if (timeLeft < 600) {
                timerElement.style.color = '#e74c3c';
            }
        }

        // إظهار صفحة محددة
        function showPage(pageNumber) {
            pages.forEach(page => {
                page.classList.remove('active');
            });
            
            document.getElementById(`page${pageNumber}`).classList.add('active');
            currentPage = pageNumber;
        }

        // تقديم الاختبار
        function submitTest() {
            clearInterval(timerInterval);
            
            // تسجيل وقت انتهاء الاختبار
            endTime = new Date();
            
            // حساب النتيجة
            const score = calculateScore();
            
            // عرض النتائج
            showResults(score);
            
            // الانتقال إلى صفحة النتائج
            showPage(3);
        }

        // حساب النتيجة
        function calculateScore() {
            let correctCount = 0;
            
            studentAnswers.forEach((answer, index) => {
                if (answer === questions[index].correctAnswer) {
                    correctCount++;
                }
            });
            
            return correctCount;
        }

        // حساب الوقت المستغرق
        function calculateTimeTaken() {
            if (!startTime || !endTime) return "غير متوفر";
            
            const timeDiff = endTime - startTime; // الفرق بالمللي ثانية
            const totalSeconds = Math.floor(timeDiff / 1000);
            const minutes = Math.floor(totalSeconds / 60);
            const seconds = totalSeconds % 60;
            
            return `${minutes} دقيقة و ${seconds} ثانية`;
        }

        // عرض النتائج
        function showResults(score) {
            const studentName = document.getElementById('studentName').value;
            const studentClass = document.getElementById('studentClass').value;
            
            // عرض معلومات الطالب
            studentInfoElement.innerHTML = `
                <h2>معلومات الطالب</h2>
                <p><strong>الاسم:</strong> ${studentName}</p>
                <p><strong>الشعبة:</strong> ${studentClass}</p>
            `;
            
            // عرض النتيجة
            const percentage = (score / questions.length) * 100;
            scoreTextElement.textContent = `النتيجة: ${score} من ${questions.length} (${percentage.toFixed(1)}%)`;
            
            // عرض الوقت المستغرق
            const timeTaken = calculateTimeTaken();
            timeTakenElement.textContent = `الوقت المستغرق: ${timeTaken}`;
            
            // عرض تفاصيل الإجابات
            resultsContainer.innerHTML = '';
            
            questions.forEach((q, index) => {
                const resultItem = document.createElement('div');
                resultItem.className = 'result-item';
                
                const userAnswer = studentAnswers[index];
                const isCorrect = userAnswer === q.correctAnswer;
                
                if (isCorrect) {
                    resultItem.classList.add('correct');
                } else {
                    resultItem.classList.add('incorrect');
                }
                
                let answerStatus = '';
                if (userAnswer === null) {
                    answerStatus = '<span style="color: orange;">لم يتم الإجابة</span>';
                } else if (isCorrect) {
                    answerStatus = '<span style="color: green;">إجابة صحيحة</span>';
                } else {
                    answerStatus = '<span style="color: red;">إجابة خاطئة</span>';
                }
                
                resultItem.innerHTML = `
                    <div class="question-number">سؤال ${index + 1}: ${q.question}</div>
                    <p><strong>إجابتك:</strong> ${userAnswer !== null ? q.options[userAnswer] : 'لم يتم الإجابة'}</p>
                    <p><strong>الإجابة الصحيحة:</strong> ${q.options[q.correctAnswer]}</p>
                    <p><strong>الحالة:</strong> ${answerStatus}</p>
                `;
                
                resultsContainer.appendChild(resultItem);
            });
        }

        // إعادة الاختبار
        function restartTest() {
            // إعادة تعيين المتغيرات
            studentAnswers = new Array(questions.length).fill(null);
            timeLeft = 50 * 60;
            currentQuestionIndex = 0;
            
            // إعادة تعيين النموذج
            document.getElementById('studentName').value = '';
            document.getElementById('studentClass').value = '';
            
            // إعادة تعيين صفحات الأسئلة
            document.querySelectorAll('.option').forEach(option => {
                option.classList.remove('selected', 'correct', 'incorrect');
            });
            
            document.querySelectorAll('.feedback').forEach(feedback => {
                feedback.textContent = '';
                feedback.className = 'feedback';
            });
            
            // العودة إلى الصفحة الأولى
            showPage(1);
        }

        // تهيئة التطبيق عند تحميل الصفحة
        document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
