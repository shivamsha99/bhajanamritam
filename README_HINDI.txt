भजनामृतम् — ऑनलाइन लॉगिन संस्करण (प्रारम्भिक)

1. config.example.js की कॉपी बनाकर उसका नाम config.js रखें।
2. config.js में अपना Supabase Project URL और sb_publishable_... key भरें।
3. Supabase SQL Editor में पहले दिया गया bhajan_songs टेबल + RLS SQL सफलतापूर्वक चल चुका होना चाहिए।
4. इस फोल्डर की सभी फाइलें HTTPS static hosting पर अपलोड करें।
5. Supabase Dashboard > Authentication > URL Configuration में Site URL और Redirect URLs में अपनी होस्ट की गई वेबसाइट का HTTPS URL जोड़ें।
6. Authentication > Providers में Email enabled और Signups enabled रखें।
7. वेबसाइट खोलकर ईमेल से रजिस्टर करें। ईमेल सत्यापन लिंक खोलें, फिर लॉगिन करें।
8. नया भजन जोड़ें। वह Supabase में user_id के साथ सेव होगा और उसी खाते से दूसरे डिवाइस पर दिखेगा।

सुरक्षा:
- केवल sb_publishable_... key फ्रंटएंड config.js में रखें।
- sb_secret_... या service_role key कभी भी वेबसाइट/ब्राउज़र में न रखें।
- RLS चालू होना और पहले बनाए गए चार user-owned policies मौजूद होना जरूरी है।
- config.js में key होने से वह ब्राउज़र में देखी जा सकती है; Publishable key का उपयोग RLS के साथ ही सुरक्षित है।

सीमाएँ:
- यह स्रोत-पैकेज है; इसे खुद से सार्वजनिक वेबसाइट पर प्रकाशित नहीं किया गया है।
- Supabase प्रोजेक्ट से जोड़ने के लिए config.js में आपके प्रोजेक्ट के वास्तविक मान भरने होंगे।
- मोबाइल और कंप्यूटर सिंक तभी होगा जब दोनों एक ही होस्ट की गई वेबसाइट पर लॉगिन करें।
- PDF निर्माण ब्राउज़र के Print > Save as PDF विकल्प से होता है।
