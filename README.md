# Secret-mission-
Mission game
import { useState } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
import { Globe, ShieldAlert, Flame } from "lucide-react";

const missions = {
  test: [
    {
      title: "رسالة من الماضي",
      description: "اكتب سر قديم واحرقه.",
      analysis: "دي أول خطوة في كسر الجدار بينك وبين حقيقتك."
    },
    {
      title: "وشك الحقيقي",
      description: "اعمل تعبير وجه غريب وصوّره.",
      analysis: "لو خفت تظهر بشكل مش مثالي، عمرك ما هتبقى حر."
    },
    {
      title: "العيون بتشوفك؟",
      description: "اقعد في مكان عام كأنك مراقب وسجل إحساسك.",
      analysis: "بتشوف إنت بتحس بإيه لما تبطل تمثل."
    },
    {
      title: "اسأل شخص غريب",
      description: "انزل اسأل شخص في الشارع سؤال غير متوقع.",
      analysis: "تجربة بتكسر التردد وتفتح التواصل العشوائي."
    }
  ],
  danger: [
    {
      title: "مهمة الصوت الممنوع",
      description: "سجل صوتك وانت بتتكلم عن خوفك.",
      analysis: "لما تسمع نفسك، بتصدق إنك موجود."
    },
    {
      title: "تحدي الحرج",
      description: "اطلب حاجة غريبة من حد في الشارع.",
      analysis: "لما تواجه الحرج، الحرج بيختفي."
    },
    {
      title: "كرر المهمة اللي خوفتك",
      description: "نفذ تاني أصعب مهمة جربتها.",
      analysis: "الإعادة هنا ختم، مش ضعف."
    },
    {
      title: "اقتحام الشخصية",
      description: "امثل شخصية خيالية وسط الناس لمدة ساعة كاملة.",
      analysis: "بتفهم أبعاد تانية لنفسك لما تخرج عن نفسك."
    },
    {
      title: "أسرار الغرباء",
      description: "اسأل ٣ غرباء عن أكتر سر مأثر في حياتهم.",
      analysis: "كل مرة تسمع سر، هتفهم العالم والناس بشكل أعمق."
    },
    {
      title: "الكرسي المكشوف",
      description: "اقعد في ميدان عام على كرسي، وارفع لافتة مكتوب عليها: 'اسألني أي حاجة'.",
      analysis: "الانفتاح بيخلي الناس تديك أكتر مما تتوقع."
    },
    {
      title: "لحظة المواجهة",
      description: "واجه شخص أذيتك أو زعلت منه بكلام مباشر وجريء.",
      analysis: "الحقيقة الصعبة أقصر طريق للحرية."
    }
  ],
  vip: [
    {
      title: "Blind Contact VR",
      description: "سلم رسالة غامضة لشخص في الشارع بدون كلام.",
      analysis: "تكسر توقعاتك عن رد فعل الناس داخل واقع شبه حقيقي."
    },
    {
      title: "اختفي ليوم VR",
      description: "عيش تجربة الاختفاء وسط قصة من 1900.",
      analysis: "تدريب على السيطرة على الذات والعزلة الداخلية."
    },
    {
      title: "فلاش باك للماضي VR",
      description: "ادخل ماضي العميل X وقت الاحتلال البريطاني.",
      analysis: "رحلة نفسية تاريخية مليئة بالغموض."
    },
    {
      title: "العملية السرية VR",
      description: "شارك في مشهد سينمائي وهمي داخل ثورة شعبية من 1900 وكأنك العميل X.",
      analysis: "تشعر إنك بطل حقيقي في مهمة أكبر منك."
    },
    {
      title: "مواجهة داخل القصر VR",
      description: "اقتحم قصر الحاكم البريطاني في مغامرة VR تكتيكية.",
      analysis: "مزيج من الحركة، التخطيط، وتحديات القرار الحاسم."
    },
    {
      title: "الهروب الكبير VR",
      description: "اهرب من سجن الاحتلال في تجربة مليئة بالإثارة.",
      analysis: "بتواجه الخوف من الفشل وتتحدى قدرتك على النجاة."
    }
  ]
};

export default function SecretMissionApp() {
  const [lang, setLang] = useState("ar");

  return (
    
      

        
🎯 Secret Mission

         setLang(lang === "ar" ? "en" : "ar")}>{lang === "ar" ? "EN" : "عربي"}
      


      
        
          Test Zone
          Danger Zone
          VIP Bomb Zone
        

        {Object.entries(missions).map(([zone, data]) => (
          
            {data.map((mission, i) => (
              
                
                  
{mission.title}

                  
{mission.description}

                  
🧠 {mission.analysis}

                
              
            ))}
          
        ))}
      
    
  );
}

