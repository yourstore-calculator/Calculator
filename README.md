<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>حاسبة النوافذ والأبواب</title>
<style>
  body {
    font-family: Arial, sans-serif;
    direction: rtl;
    max-width: 600px;
    margin: 20px auto;
    padding: 15px;
    background: #f5f7fa;
    color: #333;
  }
  h1 {
    text-align: center;
    margin-bottom: 25px;
    color: #0077cc;
  }
  label {
    display: block;
    margin: 12px 0 5px;
    font-weight: bold;
  }
  select, input[type="number"] {
    width: 100%;
    padding: 8px;
    font-size: 16px;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  input[type="checkbox"] {
    margin-left: 10px;
    transform: scale(1.3);
    vertical-align: middle;
    cursor: pointer;
  }
  button {
    margin-top: 25px;
    width: 100%;
    padding: 12px;
    font-size: 20px;
    background-color: #0077cc;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
  }
  button:hover {
    background-color: #005fa3;
  }
  .result {
    margin-top: 30px;
    padding: 15px;
    border-radius: 6px;
    background-color: #d4edda;
    color: #155724;
    font-size: 20px;
    font-weight: bold;
    text-align: center;
    display: none;
  }
</style>
</head>
<body>

<h1>حاسبة النوافذ والأبواب</h1>

<form id="calculatorForm">

  <label for="productType">نوع المنتج:</label>
  <select id="productType" required>
    <option value="">اختر نوع المنتج</option>
    <option value="نافذة">نافذة</option>
    <option value="باب">باب</option>
    <option value="أبواب متحركة">أبواب متحركة</option>
  </select>

  <!-- خيارات النوافذ -->
  <div id="windowOptions" style="display:none;">

    <label for="windowType">نوع النافذة:</label>
    <select id="windowType">
      <option value="">اختر نوع النافذة</option>
      <option value="دبل جلاس دبل فريم">دبل جلاس دبل فريم</option>
      <option value="دبل جلاس سنجل فريم">دبل جلاس سنجل فريم</option>
      <option value="سنجل جلاس سنجل فريم">سنجل جلاس سنجل فريم</option>
      <option value="نوافذ السلايدنج">نوافذ السلايدنج</option>
      <option value="نوافذ كهربائية">نوافذ كهربائية</option>
      <option value="سكاي لايت بدون المكينه">سكاي لايت بدون المكينه</option>
      <option value="سكاي لايت مع المكينه">سكاي لايت مع المكينه</option>
      <option value="الكارتن وول الثقيل">الكارتن وول الثقيل</option>
      <option value="الكارتن وول الأخف">الكارتن وول الأخف</option>
    </select>

    <label for="windowMotion">حركة النافذة:</label>
    <select id="windowMotion">
      <option value="">اختر حركة النافذة</option>
      <option value="ثابتة">ثابتة</option>
      <option value="حركة">حركة</option>
      <option value="حركتين">حركتين</option>
    </select>

    <label for="windowArea">المساحة (متر مربع):</label>
    <input type="number" id="windowArea" min="0" step="0.01" placeholder="مثلاً 1.5" />

    <label for="windowAddons">الإضافات:</label>
    <select id="windowAddons">
      <option value="بدون">بدون إضافات</option>
      <option value="شبك الباب">شبك الباب</option>
      <option value="شبك الفولدنج">شبك الفولدنج</option>
      <option value="شبك السلايد">شبك السلايد</option>
      <option value="ستارة داخلية">ستارة داخلية</option>
    </select>

  </div>

  <!-- خيارات الأبواب -->
  <div id="doorOptions" style="display:none;">

    <label for="doorType">نوع الباب:</label>
    <select id="doorType">
      <option value="">اختر نوع الباب</option>
      <option value="باب المدخل زينك">باب المدخل زينك</option>
      <option value="باب المدخل ستينلس">باب المدخل ستينلس</option>
      <option value="باب المدخل كاست المنيوم">باب المدخل كاست المنيوم</option>
      <option value="أبواب WPC فارغ">أبواب WPC فارغ</option>
      <option value="أبواب WPC مع خشب">أبواب WPC مع خشب</option>
      <option value="أبواب WPC مع حشوة ضد الصوت">أبواب WPC مع حشوة ضد الصوت</option>
      <option value="أبواب WPC مع فريم ألمينيوم">أبواب WPC مع فريم ألمينيوم</option>
      <option value="باب دورات المياه النوع الجديد">باب دورات المياه النوع الجديد</option>
      <option value="باب دورات المياه النوع الأقدم">باب دورات المياه النوع الأقدم</option>
      <option value="باب دورات المياه مخفي زجاجي">باب دورات المياه مخفي زجاجي</option>
      <option value="أبواب الألمنيوم فارغ">أبواب الألمنيوم فارغ</option>
      <option value="أبواب الألمنيوم مع خشب">أبواب الألمنيوم مع خشب</option>
      <option value="فل الألمنيوم">فل الألمنيوم</option>
      <option value="الباب المخفي">الباب المخفي</option>
      <option value="باب المنيوم خارجي">باب المنيوم خارجي</option>
      <option value="شتر دور الخارجي">شتر دور الخارجي</option>
      <option value="أبواب الحدائق الخارجيه كاست المنيوم">أبواب الحدائق الخارجيه كاست المنيوم</option>
      <option value="حواجز الدرج">حواجز الدرج</option>
      <option value="حواجز الحمام">حواجز الحمام</option>
    </select>

    <label for="doorArea">المساحة (متر مربع):</label>
    <input type="number" id="doorArea" min="0" step="0.01" placeholder="مثلاً 2.2" />

    <label><input type="checkbox" id="telbisa" /> إضافة تلبيسة للسقف (باب فقط)</label>

  </div>

  <!-- خيارات الأبواب المتحركة -->
  <div id="movingDoorOptions" style="display:none;">

    <label for="movingDoorType">نوع الباب المتحرك:</label>
    <select id="movingDoorType">
      <option value="">اختر نوع الباب المتحرك</option>
      <option value="داخلي زجاج">داخلي زجاج</option>
      <option value="داخلي متين">داخلي متين</option>
      <option value="خارجي جزء مفتوح">خارجي جزء مفتوح</option>
      <option value="خارجي جزئين مفتوحات">خارجي جزئين مفتوحات</option>
      <option value="wpc سلايد">wpc سلايد</option>
      <option value="داخلي فولدنج">داخلي فولدنج</option>
      <option value="خارجي فولدنج">خارجي فولدنج</option>
    </select>

    <label for="movingDoorArea">المساحة (متر مربع):</label>
    <input type="number" id="movingDoorArea" min="0" step="0.01" placeholder="مثلاً 2" />

    <label for="movingDoorAddon">الإضافات:</label>
    <select id="movingDoorAddon">
      <option value="بدون">بدون إضافات</option>
      <option value="ستارة">ستارة</option>
    </select>

  </div>

  <button type="submit">احسب السعر النهائي</button>
</form>

<div id="result" class="result"></div>

<script>
  const productType = document.getElementById('productType');
  const windowOptions = document.getElementById('windowOptions');
  const doorOptions = document.getElementById('doorOptions');
  const movingDoorOptions = document.getElementById('movingDoorOptions');

  // إظهار الخيارات حسب نوع المنتج
  productType.addEventListener('change', () => {
    const val = productType.value;
    windowOptions.style.display = 'none';
    doorOptions.style.display = 'none';
    movingDoorOptions.style.display = 'none';
    document.getElementById('result').style.display = 'none';

    if (val === 'نافذة') {
      windowOptions.style.display = 'block';
    } else if (val === 'باب') {
      doorOptions.style.display = 'block';
    } else if (val === 'أبواب متحركة') {
      movingDoorOptions.style.display = 'block';
    }
  });

  // أسعار النوافذ حسب النوع (بالريال/م²)
  const windowPrices = {
    "دبل جلاس دبل فريم": 58,
    "دبل جلاس سنجل فريم": 46,
    "سنجل جلاس سنجل فريم": 34,
    "نوافذ السلايدنج": 34,
    "نوافذ كهربائية": 210,
    "سكاي لايت بدون المكينه": 470,
    "سكاي لايت مع المكينه": 690,
    "الكارتن وول الثقيل": 57,
    "الكارتن وول الأخف": 31
  };

  // أسعار الأبواب حسب النوع (ريال/م²)
  const doorPrices = {
    "باب المدخل زينك": 360,
    "باب المدخل ستينلس": 360,
    "باب المدخل كاست المنيوم": 360,
    "أبواب WPC فارغ": 165,
    "أبواب WPC مع خشب": 195,
    "أبواب WPC مع حشوة ضد الصوت": 215,
    "أبواب WPC مع فريم ألمينيوم": 260,
    "باب دورات المياه النوع الجديد": 100,
    "باب دورات المياه النوع الأقدم": 90,
    "باب دورات المياه مخفي زجاجي": 100,
    "أبواب الألمنيوم فارغ": 165,
    "أبواب الألمنيوم مع خشب": 200,
    "فل الألمنيوم": 165,
    "الباب المخفي": 165,
    "باب المنيوم خارجي": 165,
    "شتر دور الخارجي": 165,
    "أبواب الحدائق الخارجيه كاست المنيوم": 165,
    "حواجز الدرج": 160,
    "حواجز الحمام": 165
  };

  // أسعار الأبواب المتحركة (ريال/م²)
  const movingDoorPrices = {
    "داخلي زجاج": 410,
    "داخلي متين": 325,
    "خارجي جزء مفتوح": 325,
    "خارجي جزئين مفتوحات": 430,
    "wpc سلايد": 230,
    "داخلي فولدنج": 270,
    "خارجي فولدنج": 320
  };

  // تكلفة الشحن لكل متر مكعب
  const shippingPerCBM = 48;

  // حساب الحجم (CBM) حسب المساحة والنوع (سماكة ثابتة لكل نوع)
  // السماكة بالامتار (مثلاً 0.05 متر)
  // لنفترض السماكة الافتراضية لكل نوع:
  const thicknessMap = {
    "نافذة": 0.06,
    "باب": 0.07,
    "أبواب متحركة": 0.07
  };

  // تكاليف الإضافات لكل منتج (ريال)
  const addonPrices = {
    "شبك الباب": 150,
    "شبك الفولدنج": 200,
    "شبك السلايد": 200,
    "ستارة داخلية": 120,
    "ستارة": 120,
    "تلبيسة السقف": 50
  };

  function calculateCBM(area, productType) {
    const thickness = thicknessMap[productType] || 0.06;
    return area * thickness; // CBM = المساحة * السماكة
  }

  function formatNumber(num) {
    return num.toLocaleString('ar-EG', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
  }

  document.getElementById('calculatorForm').addEventListener('submit', function(e) {
    e.preventDefault();

    const prodType = productType.value;
    let totalPrice = 0;
    let details = [];

    if (!prodType) {
      alert('يرجى اختيار نوع المنتج');
      return;
    }

    if (prodType === 'نافذة') {
      const type = document.getElementById('windowType').value;
      const motion = document.getElementById('windowMotion').value;
      const area = parseFloat(document.getElementById('windowArea').value);
      const addon = document.getElementById('windowAddons').value;

      if (!type || !motion || isNaN(area) || area <= 0) {
        alert('يرجى ملء جميع حقول النافذة بشكل صحيح');
        return;
      }

      // سعر المتر حسب النوع
      let unitPrice = windowPrices[type];
      if (!unitPrice) {
        alert('سعر هذا النوع من النوافذ غير متوفر');
        return;
      }

      // زيادة السعر حسب حركة النافذة
      if (motion === 'ثابتة') {
        // لا زيادة
      } else if (motion === 'حركة') {
        unitPrice *= 1.2; // زيادة 20%
      } else if (motion === 'حركتين') {
        unitPrice *= 1.35; // زيادة 35%
      }

      // حساب السعر الأساسي
      let basePrice = unitPrice * area;

      // حساب الشحن
      const cbm = calculateCBM(area, 'نافذة');
      const shippingCost = shippingPerCBM * cbm;

      totalPrice = basePrice + shippingCost;

      // إضافات
      if (addon !== 'بدون' && addonPrices[addon]) {
        totalPrice += addonPrices[addon];
        details.push(`تكلفة الإضافة (${addon}): ${formatNumber(addonPrices[addon])} ريال`);
      }

      details.unshift(`سعر الوحدة: ${formatNumber(unitPrice)} ريال/م²`);
      details.unshift(`المساحة: ${formatNumber(area)} م²`);
      details.push(`تكلفة الشحن (CBM=${formatNumber(cbm)}): ${formatNumber(shippingCost)} ريال`);

    } else if (prodType === 'باب') {
      const type = document.getElementById('doorType').value;
      let area = parseFloat(document.getElementById('doorArea').value);
      const hasTelbisa = document.getElementById('telbisa').checked;

      if (!type || isNaN(area) || area <= 0) {
        alert('يرجى ملء جميع حقول الباب بشكل صحيح');
        return;
      }

      // حسب المواصفات: الأبواب التي لها سعر ثابت على 1×2.2 متر
      const fixedSizeTypes = [
        "أبواب WPC فارغ", "أبواب WPC مع خشب", "أبواب WPC مع حشوة ضد الصوت",
        "أبواب WPC مع فريم ألمينيوم",
        "باب دورات المياه النوع الجديد", "باب دورات المياه النوع الأقدم", "باب دورات المياه مخفي زجاجي",
        "أبواب الألمنيوم فارغ", "أبواب الألمنيوم مع خشب", "فل الألمنيوم", "الباب المخفي"
      ];

      const pricePerM2 = doorPrices[type];
      if (!pricePerM2) {
        alert('سعر هذا النوع من الأبواب غير متوفر');
        return;
      }

      let basePrice = 0;

      if (fixedSizeTypes.includes(type)) {
        // السعر على 1 × 2.2 متر فقط (ثابت)
        const fixedArea = 1 * 2.2;
        basePrice = pricePerM2 * fixedArea;
      } else {
        // حساب السعر حسب المساحة الفعلية
        basePrice = pricePerM2 * area;
      }

      // حساب الشحن
      const cbm = calculateCBM(area, 'باب');
      const shippingCost = shippingPerCBM * cbm;

      totalPrice = basePrice + shippingCost;

      // إضافة تلبيسة السقف ثابتة 50 ريال (حسب طلبك)
      if (hasTelbisa) {
        totalPrice += addonPrices["تلبيسة السقف"];
        details.push(`تكلفة تلبيسة السقف: ${formatNumber(addonPrices["تلبيسة السقف"])} ريال`);
      }

      details.unshift(`سعر الوحدة: ${formatNumber(pricePerM2)} ريال/م²`);
      details.unshift(`المساحة: ${formatNumber(area)} م²`);
      details.push(`تكلفة الشحن (CBM=${formatNumber(cbm)}): ${formatNumber(shippingCost)} ريال`);
    } else if (prodType === 'أبواب متحركة') {
      const type = document.getElementById('movingDoorType').value;
      const area = parseFloat(document.getElementById('movingDoorArea').value);
      const addon = document.getElementById('movingDoorAddon').value;

      if (!type || isNaN(area) || area <= 0) {
        alert('يرجى ملء جميع حقول الأبواب المتحركة بشكل صحيح');
        return;
      }

      const unitPrice = movingDoorPrices[type];
      if (!unitPrice) {
        alert('سعر هذا النوع من الأبواب المتحركة غير متوفر');
        return;
      }

      let basePrice = unitPrice * area;

      // حساب الشحن
      const cbm = calculateCBM(area, 'أبواب متحركة');
      const shippingCost = shippingPerCBM * cbm;

      totalPrice = basePrice + shippingCost;

      // إضافات: فقط 'ستارة' أو بدون إضافات
      if (addon === 'ستارة') {
        totalPrice += addonPrices['ستارة'];
        details.push(`تكلفة الإضافة (ستارة): ${formatNumber(addonPrices['ستارة'])} ريال`);
      }

      details.unshift(`سعر الوحدة: ${formatNumber(unitPrice)} ريال/م²`);
      details.unshift(`المساحة: ${formatNumber(area)} م²`);
      details.push(`تكلفة الشحن (CBM=${formatNumber(cbm)}): ${formatNumber(shippingCost)} ريال`);
    }

    const resultDiv = document.getElementById('result');
    resultDiv.innerHTML = `
      السعر النهائي: ${formatNumber(totalPrice)} ريال <br/>
      <hr/>
      التفاصيل:<br/>
      ${details.join('<br/>')}
    `;
    resultDiv.style.display = 'block';
  });
</script>

</body>
</html>
