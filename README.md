do
    local _error = error
    error = function() os.exit() end

    local _make = gg.makeRequest
    gg.makeRequest = function(url)
        local ok, res = pcall(_make, url)
        if not ok or type(res) ~= "table" or not res.content then
            os.exit()
        end
        return res
    end

    local _load = load
    load = function(...)
        local ok, f = pcall(_load, ...)
        if not ok then os.exit() end
        return f
    end

    local _loadstring = loadstring
    if _loadstring then
        loadstring = function(...)
            local ok, f = pcall(_loadstring, ...)
            if not ok then os.exit() end
            return f
        end
    end
end
--------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------
do
    local oldRequest = gg.makeRequest
    gg.makeRequest = function(url)
        local ok, res = pcall(oldRequest, url)
        if not ok or type(res) ~= "table" or not res.content then
            os.exit()
        end
        return res
    end
end


--نطاقات Ca
gg.setVisible(false)
local cachedValues = {
    secondary = nil,
    mainPattern = nil
}

gg.alert([[
  ⭐ ━━━━━━━━━━━━━━━━━━━━━━ ⭐
 ✨   🇹🇯  🇩 🇮 🇩 🇦 🇷  🇼 🇦 🇭 🇦 🇧   🇹🇯  ✨
  ⭐ ━━━━━━━━━━━━━━━━━━━━━━ ⭐



  "العظمة ليست في أن تكون أفضل من الآخرين،
   بل في أن تكون أفضل من نفسك في الأمس."

  

    👑 🇹🇯 🅓︎ 🅘︎🅓︎🅐︎🅡︎ 🅦︎🅐︎🅗︎🅐︎🅑︎ 🇹🇯 👑 
   ⭐ ━━━━━━━━━━━━━━━━━━━━━━ ⭐
]], "البدء بقوة 🚀")




function PdaistakanyYari()

gg.setVisible(false) 
    local p2 = gg.multiChoice({
    "╔══════════ 🦋══════════╗\nꕤ 🎑             اكواد القسائم              ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🌝           جميع الملصقات           ꕤ\n╚══════════════════════╝",	
    "╔══════════ 🦋══════════╗\nꕤ 🖼️          تزويد نقاط الإطار            ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏅            اكواد السبائك               ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🧨        اكواد حدث الالوان             ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏠             اكواد الشونه                ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏔️              اكواد المنجم              ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🔶          اكواد المجوهرات            ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏖️      اكواد توسيع الاراضي          ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 👷‍♀️         اكواد فتح المباني            ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🎅   اكواد الصورة الشخصية          ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏕️            اكواد الزينة                   ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🐔  اكواد تغير شكل حيوانات         ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🛩️  تغير القطار+الميناء+الطائره    ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🏅       اكواد عددالألقاب               ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🗽   اكواد ديكورات التماثيل          ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🔰       الشاره ملف تعريفي           ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🔄            رجـــــــــــــــوع                   ꕤ\n╚══════════════════════╝",
    "╔══════════ 🦋══════════╗\nꕤ 🚪            خــــــــــــــــــرج                   ꕤ\n╚══════════════════════╝",
    
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if p2 == nil then
     gg.setVisible(true)
    return PdaistakanyYari()
    else
        if p2[1] then KobonMenu() end
        if p2[2] then Final_Emoji_Collector() end
        if p2[3] then HackItems() end
        if p2[4] then qalbAltuny() end
        if p2[5] then kandi() end
        if p2[6] then menuTools() end
        if p2[7] then StoneMenu() end   
        if p2[8] then menuYaqut() end
        if p2[9] then menuMshar() end
        if p2[10] then YellowMenu() end
        if p2[11] then Final_Auto_Collector() end
         if p2[12] then Main_Menu() end
         if p2[13] then Run_Animals_Menu() end
         if p2[14] then Run_Stations_Menu() end
         if p2[15] then NaznawakanMenu() end
         if p2[16] then Slemani_Main() end
         if p2[17] then Aram_Logokan() end
       
        
        if p2[18] then MainMenu() end
if p2[19] then
  gg.clearList()
  gg.clearResults()
  gg.toast("👋 في أمان الله، اذكرنا في صالح دعائك")
  os.exit()
end
 end

  while true do
    if gg.isVisible(true) then
      gg.setVisible(false)
      PdaistakanyYari() 
    end
    gg.sleep(100)
  end
end 

local isCouponSearched = false
local couponResults = {}

function Edit_Coupon(hex_values, name, slotIdx, totalSelected)
    if not isCouponSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber('29', gg.TYPE_DWORD)
        local results = gg.getResults(1)

        if #results < 1 then
            gg.toast(" البحث عن الكود الثاني")
            gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
            gg.searchNumber('28;1952533798;29::641', gg.TYPE_DWORD)
            gg.refineNumber('29', gg.TYPE_DWORD)
            results = gg.getResults(1)

            if #results < 1 then
                gg.toast(" البحث عن الكود الثالث")
                gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
                gg.searchNumber('65537;1970225964;29:457', gg.TYPE_DWORD)
                results = gg.getResults(1)

                if #results < 1 then
                    gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
                    gg.clearResults()
                    return false
                end
            end
        end
        couponResults = gg.getResults(1)
        isCouponSearched = true
    end

    local r = couponResults[slotIdx]
    if not r then return end

    local input = gg.prompt({"الارقام" .. name .. " اکتوب:"}, {"100"}, {"number"})
    if not input then return end

    local list = {}

    table.insert(list, {address = r.address + 12, flags = 4, value = 2, freeze = true})
    
    for i = 1, 6 do
        table.insert(list, {address = r.address + 12 + (i * 4), flags = 4, value = hex_values[i] or 0})
    end
    
    table.insert(list, {address = r.address + 40, flags = 4, value = 0})
    table.insert(list, {address = r.address + 44, flags = 4, value = tonumber(input[1])})
    
    gg.setValues(list)
    gg.addListItems(list)
    gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
end


function KobonMenu()
    gg.setVisible(false)
    local menu = gg.multiChoice({
     
        "╔══════════ 🦋══════════╗\nꕤ 🏜️             قسيمة التوسع           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🤝               قسيمة الدعم           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🏚️             قسيمة الشونة           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🏘️            قسيمة المصانع          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🚂              قسيمة القطار            ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🍇              قسيمة التاجر              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🏖️            قسيمة الجزيرة             ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🔄               تنظيف عام               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🔄              رجـــــــــــــوع                  ꕤ\n╚══════════════════════╝",

    }, {}, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if not menu then return KobonMenu() end

  
    local selected = {}
    for i = 1, 7 do if menu[i] then table.insert(selected, i) end end


    if menu[9] then 
        isCouponSearched = false
        couponResults = {}
        gg.clearResults()
        gg.clearList()
        if PdaistakanyYari then return PdaistakanyYari() end
        return
    end

    -- پاککردنەوەی گشتی
    if menu[8] then 
        isCouponSearched = false
        couponResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🎺تم تنظيف جميع النتائج")
        return KobonMenu()
    end

    -- لۆژیکی جێبەجێکردن بۆ هەر کۆبۆنێک بە جیا
    local couponConfigs = {
        [1] = {hex={0x6572661A, 0x70784565, 0x69736E61, 0x00006E6F, 0x6572661A, 0x70784565}, name="قسيمة التوسع"},
        [2] = {hex={0x756F432C, 0x4C6E6F70, 0x5464616F, 0x6E696172, 0x70726941, 0x0074726F}, name="قسيمة الدعم "},
        [3] = {hex={0x65726618, 0x626D4165, 0x6E497261, 0x00000063}, name="قسيمة الشونة"},
        [4] = {hex={0x756F4328, 0x556E6F70, 0x61726770, 0x61466564, 0x726F7463, 0x00000079}, name="قسيمة المصانع "},
        [5] = {hex={0x756F4324, 0x556E6F70, 0x61726770, 0x72546564, 0x006E6961, 0}, name="قسيمة القطار"},
        [6] = {hex={0x756F4320, 0x486E6F70, 0x44657269, 0x656C6165, 0x00000072, 0}, name="قسيمة التاجر"},
        [7] = {hex={0x756F4326, 0x556E6F70, 0x61726770, 0x73496564, 0x646E616C, 0}, name="قسيمة الجزيرة"}
    }

    for i, configIdx in ipairs(selected) do
        local config = couponConfigs[configIdx]
        Edit_Coupon(config.hex, config.name, i, #selected)
    end

    -- وەستان و دووبارە بانگکردنەوە
    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
    return KobonMenu()
end


function Final_Emoji_Collector() 
    gg.alert("⚠️ تنبيه\n\nيرجى الذهاب إلى الخانة رقم ٢٩ في الغولد باس. عندما ينتهي البحث، اضغط بسرعة وتكرار على الهدية رقم ٢٩.", "حسناً")

    
    local emoji_list = {
        3618164, 3552628, 3617140, 3158388, 3421556, 3421044, 
        3289716, 3355764, 3487092, 3290228, 3355252, 3552116,
        3223924, 3486324, 3683700, 3748980, 3289460, 3159412,
        3748724, 3420532, 3225204, 3159668, 3617652, 3683188,
        3749236, 3224948, 3486068, 3290740, 3356276, 3421812,
        3487348, 3552884, "00363170h", 3486836, "00003774h",
        3421300, 3224692, "00303170h", 3748724, 3552372,
        "00343270h", "00000033h", "00373270h", "00393170h",
        "00000032h", "00313270h", "00003370h", "00323270h",
        "00343170h", 3289972, 3159156, 3617908, "00003574h",
        3224436, "00003670h", 3158900, 3748468, 3682932,
        3551860, 3551604, "00003674h", "00003970h", "00373170h",
        "00343770h", "00003874h", "00343470h", "00003274h",
        "00333170h", "00323170h", "00003174h", "00343270h",
        "00003570h", "00003974h", "00353170h", "00303270h",
        "00003474h", "00333270h"
    }

    
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    
    local results = gg.getResults(1)
    if #results == 0 then
        gg.alert("❌ لم يتم العثور على أي خانة!")

        return
    end

    local base = results[1].address
    
    -- فریزکردنی خانەی ٣ بۆ وەرگرتنی لەسەریەک
    gg.addListItems({{address = base + 12, flags = 4, value = 2, freeze = true}})
    
    gg.toast("🚀 بدأ الدوران التلقائي للإيموجيات...")

    
    for i, code in ipairs(emoji_list) do
        gg.setValues({
            {address = base + 16, flags = 4, value = 1869440276}, -- خانەی ٤
            {address = base + 20, flags = 4, value = 1935632746}, -- خانەی ٥
            {address = base + 24, flags = 4, value = code}       -- خانەی ٦
        })
        
        gg.toast("📥 ئیمۆجی: " .. i .. " / " .. #emoji_list)
        gg.sleep(700) 
    end

    -- ✨ قۆناغی پاککردنەوەی میمۆری و لادانی فریز
    gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
    gg.sleep(1000)

    -- لادانی فریزەکان
    local list = gg.getListItems()
    if #list > 0 then
        for _, v in ipairs(list) do
            v.freeze = false
        end
        gg.addListItems(list)
    end

    -- پاککردنەوەی تەواوەتی
    gg.clearList()
    gg.clearResults()
    
    gg.alert("✅ تم تخطي جميع الإيموجيات وتفريغ الذاكرة!")
    
    if PdaistakanyYari then return PdaistakanyYari() end
end




local isHackItemsSearched = false
local hackItemsResults = {}

function HackItems()
    gg.setVisible(false) 
    local menu = gg.multiChoice({
        "╔══════════ 🦋══════════╗\nꕤ 🖼️            تزويد نقاط الإطار           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🎨            تزويد نقاط الاسم          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🙋‍♂️             اظهار حدث الأزهار        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ ↩️                   رجـــــــــــــــوع            ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🚪                    خــــــــــــروج             ꕤ\n╚══════════════════════╝",
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return HackItems() end
    
    -- ئەگەر بژاردەی سێیەم هەڵبژێررا
    if menu[3] then
        ezhar()
        return HackItems()
        
    -- ئەگەر بژاردەی چوارەم هەڵبژێررا (گەڕانەوە)
    elseif menu[4] then 
        isHackItemsSearched = false
        hackItemsResults = {}
        gg.clearResults()
        gg.clearList()
        if PdaistakanyYari then return PdaistakanyYari() end
        return 
        
    -- ئەگەر بژاردەی پێنجەم هەڵبژێررا (دەرچوون)
    elseif menu[5] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
        
    -- ئەگەر نە بژاردەی ١ و نە بژاردەی ٢ هەڵبژێردرابوون، ڕێگری لە گەڕانی هەڵە دەکەین و دەگەڕێینەوە مینۆ
    elseif not menu[1] and not menu[2] then
        return HackItems()
    end

    -- گەڕان تەنها بۆ یەکەم جار بۆ ئەم بەشە (ئەمە تەنها کاتێک کار دەکات کە بژاردەی ١ یان ٢ هەڵبژێردرابێت)
    if not isHackItemsSearched then
        gg.clearResults()
            gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
       gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isHackItemsSearched = false 
            gg.alert("❌ لم يتم العثور على أي خانة!")
            return HackItems()
        end
        hackItemsResults = gg.getResults(count)
        isHackItemsSearched = true
    end

   local input = gg.prompt({"أدخل كمية النقاط:"}, {"100"}, {"number"})
    if not input then return HackItems() end

    local toFreeze = {}
    local toEdit = {}
    local slotIdx = 1

    -- لیستی جۆرەکان
    local types = {
        {idx = 1, codes = {1634878494, 1315860327, 1416917861, 1852140399, 0, 0}}, -- Frame
        {idx = 2, codes = {1634882594, 1867148905, 1701737077, 1802458233, 28261, 0}} -- Inner Color
    }

    for _, item in ipairs(types) do
        if menu[item.idx] and hackItemsResults[slotIdx] then
            local v = hackItemsResults[slotIdx]
            
            -- فریزکردنی خانەکە
            table.insert(toFreeze, {address = v.address + 12, value = 2, flags = 4, freeze = true})
            
            -- جێگیرکردنی کۆدەکان
            for j=1, 6 do
                table.insert(toEdit, {address = v.address + 12 + (j * 4), value = item.codes[j], flags = 4})
            end
            
            table.insert(toEdit, {address = v.address + 40, value = 0, flags = 4})
            table.insert(toEdit, {address = v.address + 44, value = tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end
    
    if #toEdit > 0 then
        gg.setValues(toEdit)
        gg.addListItems(toFreeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do gg.sleep(200) end
        return HackItems()
    end
end

function ezhar()
    -- ١. دیاریکردنی مەودای یادگە بۆ ئەندرۆیدی نوێ
    gg.clearResults()
            gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
       gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('100;15;86400::29', gg.TYPE_DWORD)
        gg.refineNumber("100", gg.TYPE_DWORD)
    gg.setRanges(gg.REGION_ANONYMOUS | gg.REGION_C_ALLOC)
    
    
    local results = gg.getResultCount()
    
    if results > 0 then

        local t = gg.getResults(results)
        local validCount = 0
        local editTable = {}
        
        for i, v in ipairs(t) do
            if v.value == 100 then
               
                table.insert(editTable, {
                    address = v.address + 8, 
                    flags = gg.TYPE_DWORD,
                    value = 100
                })
                validCount = validCount + 1
            end
        end
        
if validCount > 0 then
        gg.setValues(editTable)
        gg.toast("🌸 مبروك، تم فتح حدث الأزهار والسفينة ✅")
    else
        gg.alert("لم يتم العثور على أي خانة ❌")
    end

else
    gg.alert("لم يتم العثور على أي خانة ❌")
end

    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
end





 
local isSearched = false
local config = {
    [1] = {name="برونزي", hex={0x6F72421A, 0x42657A6E, 0x696C6C75, 0x00006E6F, 0x00000000, 0x00000000}},
    [2] = {name="فضي", hex={0x6C695328, 0x42726576, 0x696C6C75, 0x6F436E6F, 0x65746E75, 0x00000072}},
    [3] = {name="ذهبي", hex={0x6C694724, 0x6C754264, 0x6E6F696C, 0x6E756F43, 0x00726574, 0x00000000}},
    [4] = {name="بلاتينيوم", hex={0x616C502C, 0x756E6974, 0x6C75426D, 0x6E6F696C, 0x6E756F43, 0x00726574}}

}

function qalbAltuny()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ 🥉       سبيكة برونزية                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🥈        سبيكة فضية                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🏅         سبيكة ذهبية                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🥈          سبيكة بلاتين                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ ??               رجــــــــوع                     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ 🚪               خـــــــروج                     ꕤ\n╚══════════════════════╝",
    
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return qalbAltuny() end

    -- ١. گەڕانەوە و پاککردنەوەی تەواوی میمۆری
    if menu[5] then 
        isSearched = false
        gg.clearResults()
        gg.clearList()
        gg.toast("🔄 تم تفريغ الذاكرة")
        if PdaistakanyYari then return PdaistakanyYari() end 
        return 
    end

    if menu[6] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end
    
    local selected = false
    for i=1, 4 do if menu[i] then selected = true break end end
    if not selected then return qalbAltuny() end

    if not isSearched then
        
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        isSearched = true
    end

    local count = gg.getResultCount()
    if count == 0 then 
        isSearched = false 
gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")


        return qalbAltuny()
    end

    local res = gg.getResults(count)
local input = gg.prompt({'أدخل الكمية المطلوبة:'}, {'0'}, {'number'})
    if input == nil then return qalbAltuny() end

    gg.clearList()
    local edit = {}
    local freeze = {}

    -- ٢. ڕێگری لە تێکەڵبوونی کۆد بە بەکارهێنانی slotIndex
    local slotIndex = 1
    for i = 1, 4 do
        if menu[i] and res[slotIndex] then
            local v = config[i]
            local r = res[slotIndex]
            
            -- جێگیرکردنی خانەکە
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            
            -- دانانی هێکسەکان
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            
            -- بڕی هەدیەکە
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = input[1], flags = 4})
            
            slotIndex = slotIndex + 1 -- هەر جۆرە قاڵبێک یەک خانەی جیاواز دەگرێت
        end
    end
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end
        return qalbAltuny() 
    else
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن")
        return qalbAltuny() 
    end
end

-- بەکارهێنانی ناوی جیاواز بۆ ئەوەی تێکەڵی بەشەکانی تر نەبێت
local isNailSearched = false
local nailResults = {}

local nailConfig = {
        [1] = {name="مسمار", hex={0x69616E0E, 0x74614D6C, 0, 0, 0, 0}},
        [2] = {name="دلو", hex={0x69617016, 0x6552746E, 0x74614D64, 0, 0, 0}},
        [3] = {name="مطرقة", hex={1835100178, 1299342701, 29793, 0, 0, 0}}

}

function menuTools()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ       📌      اکواد مسمار                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ       🪣     اکواد طلاء أحمر             ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ       🔨      اكواد مطرقة                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ       🔄      رجـــــــــوع                       ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ        🚪       خــــــــروج                      ꕤ\n╚══════════════════════╝",
     
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return menuTools() end

    -- گرنگترین بەش: کاتێک دەگەڕێیتەوە، هەموو ئەنجامە کۆنەکان بسڕەوە
    if menu[4] then 
        isNailSearched = false
        nailResults = {}
        gg.clearResults() -- پاککردنەوەی لیستی گەڕان بۆ ئەوەی تێکەڵی کاندی نەبێت
        if PdaistakanyYari then return PdaistakanyYari() end
        return 
    end

    if menu[5] then os.exit() end

    -- پشکنین ئایا هیچ کام لە کەرەستەکان هەڵبژێردراوە؟
    local selected = {}
    for i=1, 3 do if menu[i] then table.insert(selected, i) end end
    if #selected == 0 then return menuTools() end

    -- لێرەدا، ئەگەر تازە چوویتە ناو بەشەکە، گەڕانی کۆن بەتەواوی پاک دەکەینەوە
    if not isNailSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isNailSearched = false 
            gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن.") 
            return menuTools()
        end
        nailResults = gg.getResults(count)
        isNailSearched = true
    end

    local input = gg.prompt({'أدخل الكمية المطلوبة:'}, {'0'}, {'number'})    
    if input == nil then return menuTools() end

    local edit, freeze = {}, {}
    local slotIdx = 1

    -- دابەشکردنی کەرەستەکان بەسەر خانەکاندا بەبێ تێکەڵبوون
    for _, idx in ipairs(selected) do
        if nailResults[slotIdx] then
            local v = nailConfig[idx]
            local r = nailResults[slotIdx]
            
            -- بەکارهێنانی freeze بۆ جێگیرکردنی جۆری خانەکە
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            
            -- گۆڕینی هێکسەکان بۆ کەرەستەی نوێ
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            
            -- دانانی بڕی پێویست
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do gg.sleep(200) end
        return menuTools() 
    end
end


-- ١. گۆڕاوەکان و ڕێکخستنی هێکسەکان
local isKandiSearched = false
local kandiResults = {}
local kandiConfig = {
    [1] = {name="كرة ملونة", hex={1379101978, 1651403105, 1631745903, 27756, 0, 0}},
    [2] = {name="متفجرات", hex={1110666508, 6450543, 11, 0, 2105761864, 117}},
    [3] = {name="صاروخ", hex={1278438668, 6647401, 11, 0, 2105761864, 117}},
    [4] = {name="مطرقة شجاعة", hex={1295215888, 1701604449, 116, 0, 0, 0}},
    [5] = {name="حفارة (دريل)", hex={1211329824, 2053730927, 1635020399, 1852394604, 101, 0}},
    [6] = {name="وزن ثقيل", hex={1446210844, 1769239141, 1282171235, 6647401, 0, 0}},
    [7] = {name="مروحة", hex={1379101974, 1969779557, 1701602918, 0, 0, 0}}

}

-- ٢. فانکشنی سەرەکی کاندی
function kandi()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🌝          كرة ملونة                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ      🧨         الديناميت                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚀             صاروخ                     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧛              مثقاب                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧛‍♂️        مطرقة ثاقبة                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🤖                ثقل                      ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🤗               مروحة                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄          رجـــــــــوع                     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪          خــــــــروج                     ꕤ\n╚══════════════════════╝",

    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return kandi() end

    -- گەڕانەوە: تەنها لێرە میمۆری بە تەواوی پاک دەبێتەوە
    if menu[8] then
        isKandiSearched = false
        kandiResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
        if PdaistakanyYari then return PdaistakanyYari() end
        return
    end

    if menu[9] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end

    -- پشکنینی هەڵبژاردن
    local anySelected = false
    for i=1, 7 do if menu[i] then anySelected = true break end end
    if not anySelected then return kandi() end

    -- گەڕان تەنها جارێک دەکرێت تا دوگمەی گەڕانەوە دانەنێیت
    if not isKandiSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isKandiSearched = false
            gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
            return kandi()
        end
        kandiResults = gg.getResults(count)
        isKandiSearched = true
    end

   local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
    if input == nil then return kandi() end

    local edit = {}
    local freeze = {}

    -- دابەشکردنی کاندییەکان بەسەر خانەکاندا بۆ ڕێگری لە تێکەڵبوون
    local slotIdx = 1
    for i = 1, 7 do
        if menu[i] and kandiResults[slotIdx] then
            local v = kandiConfig[i]
            local r = kandiResults[slotIdx]
            
            -- فریزکردنی خانەکە
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            
            -- دانانی هێکسەکان
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            
            -- ڕێکخستنی بڕ
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = input[1], flags = 4})
            
            slotIdx = slotIdx + 1 -- دەچێتە سەر خانەی دوواتر بۆ بژاردەی دوواتر
        end
    end 
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        -- شاردنەوەی مێنۆ تا کلیک لە ئایکۆنی جێم جاردن دەکەیتەوە
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end
        
        return kandi() 
    else
        Gg.alert("❌ لم يتم إجراء أي تغيير!")
        return kandi() 
    end
end




--[[ ✨ SEROK ARAM LUXURY - YAQUT ONLY ✨ ]]--

-- ١. گۆڕاوەکان (جیاواز بۆ ئەوەی تێکەڵ نەبێت)
local isYaqutSearched = false
local yaqutResults = {}
local yaqutConfig = {
    [1] = {name="الزمرد الأخضر", hex={0x6D656708, 0x00000032, 0, 0, 0, 0}},
    [2] = {name="الياقوت الأصفر", hex={0x6D656708, 0x00000031, 0, 0, 0, 0}},
    [3] = {name="الياقوت الأحمر", hex={0x6D656708, 0x00000033, 0, 0, 0, 0}}

}

-- ٢. فانکشنی سەرەکی یاقوتەکان
function menuYaqut()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🟢       الزمرد الأخضر                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🟡      الياقوت الأصفر               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔴      الياقوت الأحمر               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄           رجــــــوع                      ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪           خــــــروج                     ꕤ\n╚══════════════════════╝",
   
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return menuYaqut() end

    -- گەڕانەوە: پاککردنەوەی میمۆری بۆ بەشەکانی تر
    if menu[4] then
        isYaqutSearched = false
        yaqutResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
        if PdaistakanyYari then return PdaistakanyYari() end
        return
    end

    if menu[5] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end
    
    -- پشکنینی هەڵبژاردن
    local anySelected = false
    for i=1, 3 do if menu[i] then anySelected = true break end end
    if not anySelected then return menuYaqut() end

    -- گەڕان تەنها یەکجار تا کاتی گەڕانەوە
    if not isYaqutSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isYaqutSearched = false 
            gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
            return menuYaqut()
        end
        yaqutResults = gg.getResults(count)
        isYaqutSearched = true
    end

    local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
    if input == nil then return menuYaqut() end

    local edit = {}
    local freeze = {}

    -- لۆژیکی ڕێگری لە تێکەڵبوونی یاقوتەکان
    local slotIdx = 1
    for i = 1, 3 do
        if menu[i] and yaqutResults[slotIdx] then
            local v = yaqutConfig[i]
            local r = yaqutResults[slotIdx]
            
            -- فریزکردنی خانەکە
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            
            -- دانانی هێکسەکان
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            
            -- ڕێکخستنی بڕ
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end 
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end 
        return menuYaqut() 
    else
        Gg.alert("❌ لم يتم إجراء أي تغيير!")
        return menuYaqut()
    end
end


--[[ 🛠️ SEROK ARAM LUXURY - EXPANSION TOOLS 🛠️ ]]--
local isExpansionSearched = false
local expansionResults = {}
local expansionConfig = {
    [1] = {name="فأس 🪓", hex={0x65786106, 0, 0, 0, 0, 0}},
    [2] = {name="مجرفة 🧹", hex={0x63697008, 0x4265006B, 0x696C6C75, 0x6F436E6F, 0x65746E75, 0x00000072}},
    [3] = {name="منشار 🪚", hex={0x544E5406, 0x42657A00, 0x696C6C75, 0x6F436E6F, 0x65746E75, 0x00000072}}

}

-- ٢. فانکشنی مەنیوی تەور و مشار
function menuMshar()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🪓        اكواد فأس                    ꕤ\n╚══════════════════════╝",
       "╔══════════ 🦋══════════╗\nꕤ     🧹        اكواد معول                  ꕤ\n╚══════════════════════╝",
       "╔══════════ 🦋══════════╗\nꕤ     🪚         اكواد منشار                  ꕤ\n╚══════════════════════╝",
       "╔══════════ 🦋══════════╗\nꕤ     🔄          رجـــــــــوع                     ꕤ\n╚══════════════════════╝",
       "╔══════════ 🦋══════════╗\nꕤ     🚪           خـــــــروج                     ꕤ\n╚══════════════════════╝",

    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return menuMshar() end

    -- گەڕانەوە و پاککردنەوەی میمۆری
    if menu[4] then
        isExpansionSearched = false
        expansionResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
        if PdaistakanyYari then return PdaistakanyYari() end
        return
    end

    if menu[5] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end

    -- پشکنین بۆ هەڵبژاردن
    local anySelected = false
    for i=1, 3 do if menu[i] then anySelected = true break end end
    if not anySelected then return menuMshar() end

    -- گەڕان تەنها یەکجار
    if not isExpansionSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isExpansionSearched = false 
            gg.alert("❌ دڵنیابەوە لە یاری بە سراوەتەوە بە جێم ") 
            return menuMshar()
        end
        expansionResults = gg.getResults(count)
        isExpansionSearched = true
    end

    local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
    if input == nil then return menuMshar() end

    local edit = {}
    local freeze = {}

    -- لۆژیکی ڕێگری لە تێکەڵبوونی کۆد
    local slotIdx = 1
    for i = 1, 3 do
        if menu[i] and expansionResults[slotIdx] then
            local v = expansionConfig[i]
            local r = expansionResults[slotIdx]
            
            -- فریزکردنی خانەکە
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            
            -- دانانی هێکسەکان
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            
            -- بڕی کەرەستەکە
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end 
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end 
        return menuMshar() 
    else
        Gg.alert("❌ لم يتم إجراء أي تغيير!")
        return menuMshar()
    end
end


function Final_Auto_Collector()
    
    -- لیستی هەموو کۆدەکان
    local all_avatars = {
        3748147, 3291442, 3553329, 3289393, 3487793, 3618865, 3551281, 3355697, 
        3160370, 3552050, 3159090, 3749681, 3290161, 3160113, 3618353, 3225139, 
        3618611, 3356723, 3356467, 3553331, 3487795, 3422259, 3291187, 3553075, 
        3749170, 3683634, 3224882, 3290418, 3421234, 3619121, 3684657, 3750193, 
        3158066, 3223602, 3289138, 3683889, 3290929, 3684401, 3354674, 3682610, 
        3551538, 3223858, 3356977, 3291441, 3225649, 3486514, 3420466, 3289394, 
        3616818, 3291442, 3422257, 3618609, 3553073, 3487537, 3552306, 3683378, 
        3682609, 3486257, 3551793, 3617329, 3682865, 3748401, 3289905, 3355441, 
        3486513, 3552049, 3683121, 3159089, 3291186, 3618866, 3289907, 3748403, 
        3552307, 3159347, 3159091, 3421235, 3552051, 3618099, 3683123, 3224627, 
        3420979, 3551795, 3420978, 3289906, 3553586, 3684658, 3748147, 3158579, 
        3289651, 3355187, 3420723, 3682867, 3224371, 3289907, 3684147, 3225651, 
        3291443, 3422515, 3486770, 3421490, 3552562, 3487026, 3618098, 3749426, 
        3553074, 3422258, 3487794, 3684402, 3422513, 3617074, 3355186, 3682866, 
        3617585, 3749169
    }

    -- گەڕان بۆ خانەی ٢٩
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    
    local results = gg.getResults(1)
    if #results == 0 then return gg.alert("❌ دڵنیابەوە لە یاری بە سراوەتەوە بە جێم ") end
    
    local address29 = results[1].address
    local cell3 = address29 + 12
    
    -- فریزکردنی خانەی ٣
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    gg.toast("🚀 بدأت عملية " .. #all_avatars .. " صور!")
    
    for i, code in ipairs(all_avatars) do
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = 1635148044},
            {address = cell3 + 8,  flags = 4, value = code},
            {address = cell3 + 12, flags = 4, value = 0},
            {address = cell3 + 16, flags = 4, value = 0},
            {address = cell3 + 20, flags = 4, value = 0},
            {address = cell3 + 24, flags = 4, value = 0}
        })
        
        gg.toast("🎁 صورة [" .. i .. "] نشطة")
        gg.sleep(800) 
    end

    -- ✨ قۆناغی پاککردنەوەی میمۆری و فریز (Memory Cleanup)
    gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
    
    -- لادانی هەموو فریزەکان
    local list = gg.getListItems()
    if #list > 0 then
        for _, v in ipairs(list) do
            v.freeze = false
        end
        gg.addListItems(list) -- نوێکردنەوەی لیستەکە بەبێ فریز
    end

    -- سڕینەوەی هەموو لیستەکە و ئەنجامی گەڕانەکان
    gg.clearList()
    gg.clearResults()
    
    gg.alert("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
    
    if PdaistakanyYari then return PdaistakanyYari() end
end

--[[ 🏆 SEROK ARAM LUXURY - YELLOW ITEMS 🏆 ]]--

local isYellowSearched = false
local yellowResults = {}
local yellowConfig = {
    [1] = {name="📦 بلوك", hex={0x6972420A, 0x42006B63, 0x696C6C75, 0x6F436E6F, 0x65746E75, 0x00000072}},
    [2] = {name="📏 لوح", hex={0x696C500A, 0x42006174, 0x696C6C75, 0x6F436E6F, 0x65746E75, 0x00000072}},
    [3] = {name="💎 زجاج", hex={0x616C470A, 0x00007373, 0, 0, 0, 0}},
    [4] = {name="⚙️ منشار دائري", hex={0x776F7010, 0x61737265, 0x00000077, 0, 0, 0}},
    [5] = {name="⚡ مثقاب كهربائي كبير", hex={0x63616A14, 0x6D61686B, 0x0072656D, 0, 0, 0}},
    [6] = {name="🛠️ مثقاب", hex={0x6972640A, 0x61006C6C, 0x00000077, 0, 0, 0}}

}

function YellowMenu()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     📦         اکواد طابوق                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     📏         اکواد بلاط                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🪟         اكواد زجاج                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ⚙️       منشار كهربائي               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ☄️        مطرقة ثاقبة                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧬         اكواد مثقاب                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄         رجــــــــــوع                     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪         خــــــــــروج                     ꕤ\n╚══════════════════════╝",
   
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return YellowMenu() end

    -- گەڕانەوە: پاککردنەوەی میمۆری
    if menu[7] then
        isYellowSearched = false
        yellowResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
        if PdaistakanyYari then return PdaistakanyYari() end
        return
    end

    if menu[8] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end
    
    -- پشکنینی هەڵبژاردن
    local anySelected = false
    for i=1, 6 do if menu[i] then anySelected = true break end end
    if not anySelected then return YellowMenu() end

    -- گەڕان تەنها یەکجار
    if not isYellowSearched then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isYellowSearched = false 
            gg.alert("❌ تکایە دڵنیابە لەیاریەکە بەسراوەنەوە بە جێم ") 
            return YellowMenu()
        end
        yellowResults = gg.getResults(count)
        isYellowSearched = true
    end

    local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
    if not input then return YellowMenu() end

    local edit, freeze = {}, {}
    
    -- لۆژیکی ڕێگری لە تێکەڵبوونی کۆد
    local slotIdx = 1
    for i = 1, 6 do
        if menu[i] and yellowResults[slotIdx] then
            local v = yellowConfig[i]
            local r = yellowResults[slotIdx]
            
            table.insert(freeze, {address=r.address+12, value=2, flags=4, freeze=true})
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address=r.address+12+(j*4), value=h, flags=4}) 
            end
            table.insert(edit, {address=r.address+40, value=0, flags=4})
            table.insert(edit, {address=r.address+44, value=tonumber(input[1]), flags=4})
            
            slotIdx = slotIdx + 1
        end
    end
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end 
        return YellowMenu() 
    else
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return YellowMenu()
    end
end

-- 1. لیستی کۆدەکان (بەشی دڵ و ورچەکان بە تەواوی دانراوە)





-- 2. مێژوو و ناو نیشانی سەرەکی
function Main_Menu()

gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     ❄️           اكواد ثلج                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🦋        مجموعة زينة               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🌊       مجموعة اكواد ما          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ⛲    مجموعة اكواد نافورة       ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧸        ​القلوب والدببة              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧟‍♀️         منزل الساحرا                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🌲      اکواد الأشجار                  ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🐰         منزل الأرانب                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚧              السیاج                    ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄         رجــــــــــــــوع                   ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

if menu == nil then 
    gg.setVisible(false) -- مێنووەکە دەشارێتەوە
    
    -- ئەم بەشە سکرێپتەکە دەخەوێنێت هەتا خۆت کلیک لە گەیم جاردن دەکەیتەوە
    while true do
        if gg.isVisible() then
            gg.setVisible(false)
            return Main_Menu() -- کاتێک خۆت کلیکت کردەوە، ئینجا مێنووەکە پیشان دەدات
        end
        gg.sleep(100) -- بۆ ئەوەی لۆد لەسەر مۆبایلەکە دروست نەبێت
    end
end
    
    if menu[1] then Ice_InitialSetup() end 
    if menu[2] then Run_Decoration() end
    if menu[3] then Run_Water_Decoration() end
    if menu[4] then Run_Fountain() end
    if menu[5] then Run_Hearts_Bears() end
    if menu[6] then Run_Witch_Houses()end 
    if menu[7] then Run_Trees()end 
    if menu[8] then Run_Rabbit_Houses()end 
    if menu[9] then Run_Fences()end 
    -- بەشەکانی تر لێرە بانگ دەکرێن...
    
    if menu[10] then PdaistakanyYari() end
end

-- SEROK ARAM - ICE COLLECTION (MANUAL & KURDI)
gg.setVisible(false)

local ice_target = nil
local ice_isReady = false
local selectedIceIndex = 0

local ice_collection = {
        {name = "حمام ساخن (1) 🛁", codes = {0x6563691C, 0x68637241, 0x6372615F, 0x00636974, 0, 0}},
    {name = "ينابيع مياه ساخنة ♨️", codes = {0x746F6820, 0x69727053, 0x6D5F676E, 0x68637461, 0x33, 0}},
    {name = "جسر لشخصين 🌉", codes = {1919435562, 1836348265, 1918137185, 1601071457, 1684632130, 25959}},
    {name = "سوق شجرة رأس السنة 🌲", codes = {1701991446, 1632460645, 1952803698, 0, 672503271, 110}},
    {name = "أدوات رياضية ⛷️", codes = {1768641296, 1869108063, 672268400, 110, 672503271, 110}},
    {name = "ديكور تنين الجليد 🐉", codes = {0x65636912, 0x67617244, 0x00006E6F, 0, 0, 0}},
    {name = "زلاقة الأغنام (1) 🐑", codes = {1701335828, 1817407589, 6644841, 0, 0, 0}},
    {name = "ورشة الإصلاح 🛠️", codes = {0x61656220, 0x5F797475, 0x5F666C65, 0x73756F68, 0x65, 0}},
    {name = "ليلة رأس السنة 🎆", codes = {0x61656224, 0x5F797475, 0x746E6173, 0x6C705F61, 0x6B6E, 0}},
    {name = "فوانيس 🏮", codes = {0x72757422, 0x6C736F62, 0x65676465, 0x6E61735F, 0x6174, 0}},
    {name = "ساحة التزلج ⛸️", codes = {0x6D6F721A, 0x635F6E61, 0x69726168, 0x746F, 0, 0}},
    {name = "زلاقة الكلاب 🐕", codes = {0x726F771A, 0x6F68736B, 0x61724370, 0x6873, 0, 0}},
    {name = "المحطة القطبية ❄️", codes = {0x73616C1C, 0x756F4874, 0x6C705F72, 0x6B6E, 0, 0}},
    {name = "نهر جليدي 🌊", codes = {0x796C6620, 0x746E614C, 0x5F6E7265, 0x746E6173, 0x61, 0}},
    {name = "منزل جليدي (إيجلو) 🏠", codes = {0x6165622C, 0x5F797475, 0x74616B73, 0x50676E69, 0x75676E65, 0x736E69}},
    {name = "موسم الأعياد 🎊", codes = {1886930220, 1953064037, 1148088169, 1919902565, 1869182049, 3486318}},
    {name = "الماموث الكبير (فيل) 🐘", codes = {1835101468, 1752461165, 1952542047, 3369059, 0, 0}},
    {name = "كوخ استراحة العيد 🏡", codes = {1852405542, 1500669300, 1601466997, 1935764856, 842149938, 0}},
    {name = "متجر الهدايا 🎁", codes = {1919435548, 1836348265, 1130328929, 6645345, 0, 0}},
    {name = "حلبة التزلج الكردية ⛸️", codes = {1734960684, 1399157365, 1769234795, 2019518318, 846422381, 3289648}},
    {name = "معركة كرات الثلج ☃️", codes = {1869509406, 1734952567, 1885303912, 1802396012, 0, 0}},
    {name = "متعة الشتاء ❄️", codes = {1634034216, 1601795189, 1953393015, 1667199589, 1869508193, 110}},
    {name = "نافورة جليدية ⛲", codes = {1634034220, 1601795189, 1836674127, 1180920176, 1953396079, 7235937}},
    {name = "منزل ضفة البحيرة 🏖️", codes = {1634034210, 1601795189, 1701536108, 1970235487, 1912628595, 116}},
    {name = "تميمة النصر 🏆", codes = {1768649504, 2003780467, 2037149535, 1634300013, -1699151772, 113}},
    {name = "ساحة الألعاب 🎢", codes = {1634034218, 1601795189, 2003791475, 1601069421, 1952541555, 29285}},
    {name = "كرة ثلجية (Snowball) 🔮", codes = {1919443748, 1836348265, 1935635297, 1651994478, 7105633, 0}},
    {name = "ملك الجليد 👑", codes = {1919435550, 1836348265, 1633645409, 1818584942, 271805952, 0}},
    {name = "حديقة الشتاء المائية 🐳", codes = {1634034220, 1601795189, 1650811753, 1600615013, 1735288176, 7235957}},
    {name = "قلعة جليدية 🏰", codes = {1634034214, 1601795189, 2003791475, 1953656678, 1936942450, 0}},
    {name = "زلاقة الأغنام (2) 🐑", codes = {0x65685314, 0x6C537065, 0x656469, 0, 0, 0}},
    {name = "أزقة سحرية ✨", codes = {0x7268631E, 0x6D747369, 0x745F7361, 0x6E696172, 0, 0}},
    {name = "القلعة المتجمدة 🏔️", codes = {1634034210, 1601795189, 1600480105, 1953718627, 25964, 0}},
    {name = "كوخ رجل الثلج ⛄", codes = {0x6169471A, 0x535F746E, 0x6D776F6E, 0x616E, 0, 0}},
    {name = "مصعد التزلج 🚠", codes = {1634034220, 1601795189, 1852732786, 1667199589, 1701601889, 7496035}}
}

function Ice_InitialSetup()
    gg.toast("🦜 البحث مستمر، يرجى الانتظار 🦜")
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local r = gg.getResults(1)
    if #r == 0 then 
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        PdaistakanyYari()
        return false 
    end
    ice_target = r[1].address + 12
    gg.addListItems({{address = ice_target, flags = 4, value = 2, freeze = true}})
    ice_isReady = true
    Ice_Menu() -- بانگی لیستەکە دەکات دوای گەڕان
    return true
end -- ئەمە دێڕی ١٠٦٤ دەبێت


function ApplyIce(index)
    if not ice_isReady then return end
    local codes = ice_collection[index].codes
    gg.setValues({
        {address = ice_target + 4,  flags = 4, value = codes[1]},
        {address = ice_target + 8,  flags = 4, value = codes[2]},
        {address = ice_target + 12, flags = 4, value = codes[3]},
        {address = ice_target + 16, flags = 4, value = codes[4]},
        {address = ice_target + 20, flags = 4, value = codes[5]},
        {address = ice_target + 24, flags = 4, value = codes[6]}
    })
    gg.toast("❄️ تم التفعيل: " .. ice_collection[index].name)
end

function Ice_Menu()
    if not ice_isReady then if not Ice_InitialSetup() then return end end
    
    local names = {}
    for i, v in ipairs(ice_collection) do
        names[i] = (selectedIceIndex == i and "🔘 " or "⚪ ") .. v.name
    end
    table.insert(names, "خروج 🔙")

    gg.setVisible(false) -- لێرەدا مینۆکە دەشارێتەوە بۆ ئەوەی ڕێگەت بدات دیارییەکە وەربگریت
    local choice = gg.choice(names, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋\n╚══════════════════════╝")

    -- ١. ئەگەر پەنجەت لە دەرەوە دا (Cancel)
    if choice == nil then 
        -- لێرەدا سکرێپتەکە "سلیپ" دەکات و ناچێتەوە مینۆی سەرەکی
        return Ice_Menu() 
    end
    
    -- ٢. گەڕانەوە بۆ مینۆی سەرەکی
    if choice == #names then 
        Main_Menu() 
        return 
    end

    -- ٣. چالاککردنی دیارییەکە
    selectedIceIndex = choice
    ApplyIce(choice) 
    
    -- ٤. لێرەدا دەتوانی ماوەیەک "سلیپ" دابنێیت (بۆ نموونە ٢ چرکە)
    gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
    gg.sleep(2500) 
    
    -- دوای سلیپەکە، دووبارە مینۆکە نیشان دەداتەوە
    return Ice_Menu() 
end


-- ١. لیستی کۆدەکان (وەک خۆی جێگیر کراوە)
local heart_and_bears = {
    {1919435554, 1836348265, 1818194785, 1702129249, 67137138, 113},        -- ستوونی ڕووناکی جەژن
    {1818318380, 1769238117, 1885300078, 1868916585, 1818194798, 6649455}, -- کۆتری عاشق
    {1818318380, 1769238117, 1751082350, 1953653093, 1632136777, 7562350}, -- خۆشەویستی نەمڕ
    {1818318378, 1769238117, 1784636782, 1299477365, 1769108065, 25701},   -- بوک و زاوا
    {1818318380, 1769238117, 1818191214, 1919252079, 1700945779, 6841198}, -- کورسی خۆشەویستان
    {1818318378, 1769238117, 1415538030, 2036622437, 1634034271, 12914},   -- ورچی یاری
    {1818318372, 1769238117, 1935631726, 1852142181, 6644833, 113},        -- ژوانێکی ڕۆمانسی
    {1818318378, 1769238117, 1818191214, 1919252079, 1633902451, 29810},   -- عەرەبانەی گوڵ
    {1701860140, 1818323299, 1969317186, 1113553268, 1766876517, 7630700}, -- هەنگە فڕیوەکە
    {1869375000, 1601332599, 1852405619, 103, 0, 0},                       -- جۆلانەی گوڵ
    {1818318374, 1769238117, 1717527918, 1702326124, 1684365938, 0},       -- باخچەی گوڵ
    {1869115432, 1951625076, 1600417377, 1701601654, 1852404846, 101},     -- شوێنی وێنەی هاوسەران
    {1818318378, 1769238117, 1130325358, 1684631669, 1920090483, 30575},   -- تیری کیوبید
    {1818318362, 1769238117, 1801413998, 31077, 0, 0},                     -- کلیلی دڵ
    {1818318374, 1769238117, 1885300078, 1752397164, 1952539487, 0},       -- پشیلەی خۆشەویست
    {1818318366, 1769238117, 1113548142, 2037280373, 0, 0},                -- کەروێشکی یاری
    {1818318374, 1769238117, 1885300078, 1937011567, 1885693288, 0},       -- گۆڕەپانی سەمای گوڵ
    {1634034210, 1683974243, 1701015137, 1869375071, 1879077487, 7631471}, -- هۆڵی ناوداران
    {1818318376, 1769238117, 1415538030, 2036622437, 1634034271, 114}      -- ورچی یاری ٢
}

local selectedHeartIndex = 0

-- ٢. فەنکشنی سەرەکی بە شێوازی مینۆ و قفلکراو
function Run_Hearts_Bears()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تکایە دڵنیابەوە لەوەی یاری بەسراوەتەوە بە جێم ") 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Heart_Menu_Loop()
        local names = {
          "عمود أضواء العيد", "حمامة العشاق", "الحب الأبدي", "العريس والعروس", 
"كرسي العشاق", "دب اللعبة", "موعد رومانسي", "عربة الزهور", 
"النحلة الطائرة", "أرجوحة الزهور", "حديقة الزهور", "مكان تصوير الأزواج", 
"سهم كيوبيد", "مفتاح القلب", "القط الودود", "أرنب اللعبة", 
"ساحة رقص الزهور", "قاعة المشاهير", "دب اللعبة 2"
        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedHeartIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "خروج 🔙")

        -- شاردنەوەی گەیم گواردیان لە پشت مینۆکە
        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        -- قفلکردن: ئەگەر پەنجە لە دەرەوە بدات، دەرناچێت
        if choice == nil then 
            return Heart_Menu_Loop() 
        end
        
        -- گەڕانەوە بۆ مینۆی سەرەکی
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        -- چالاککردنی دیارییەکە
        selectedHeartIndex = choice
        local codes = heart_and_bears[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        
        -- سلیپ بۆ ئەوەی یارییەکە لاگ نەکات و هەدیەکە جێگیر بێت
        gg.sleep(2500) 
        
        -- دووبارە بانگکردنەوە بۆ ئەوەی لە مینۆکە نەیەتە دەرەوە
        return Heart_Menu_Loop() 
    end

    -- دەستپێکردن
    Heart_Menu_Loop()
end

-- ١. لیستی کۆدەکان بە ناوی کوردییەوە
local decoration_collection = {
    {1918984988, 1702065519, 1701338988, 7891308, 2040695907, 122}, -- ئەسپە فڕیوەکان
    {1852394266, 1836016743, 1953391939, 25970, 0, 0},             -- ناوەندی شانشین
    {1634034208, 1601795189, 1718773107, 1869574239, 108, 0},      -- یاری سەر ئاو
    {1634879254, 1348429168, 1936942450, 0, 672503271, 110},       -- گوشەری ترێ
    {1818585130, 1333028205, 1886352483, 1633645429, 1701405550, 29806}, -- گوشەری ترێ ٢
    {1852395544, 1819632467, 1920300144, 101, 2040695907, 122},    -- سێوی کارامێل
    {0x7261671C, 0x736E6564, 0x6172615F, 0x00636962, 0, 0},        -- تەنافی جل
    {1634034216, 1601795189, 1970169206, 1818648435, 1634890873, 112}, -- دیکۆری تایبەت
    {1818585130, 1333028205, 1886352483, 1633645429, 1701405550, 29806}, -- ڕووەکی گۆشتخۆر
    {0x69617318, 0x676E696C, 0x6361725F, 0x00000065, 0, 0},        -- پاسکیل سواری
    {0x746F4816, 0x53676F44, 0x676E6977, 0, 0, 0},                 -- جۆلانەی هۆت دۆگ
    {0x6E61632A, 0x72547964, 0x5F6E6961, 0x66727573, 0x65676E69, 0x00007372}, -- شەمەندەفەری شیرینی
    {0x61656224, 0x5F797475, 0x676E756A, 0x6D5F656C, 0x006B6E6F, 0}, -- درەختی مۆز
    {1969320740, 1701273971, 1936028255, 1634889588, 7499636, 116}, -- باشترین سەروو
    {1869366808, 1601332599, 1919906899, 101, 0, 0},               -- فرۆشگای گوڵ
    {1986085652, 1817206629, 6644577, 116, 0, 0},                  -- ئەشکەوتی ئارامی
    {1634034220, 1601795189, 1634497633, 1936290926, 1635021663, 6649204}, -- پێشانگای وێنە
    {0x6165622A, 0x5F797475, 0x616C7461, 0x7369746E, 0x61725F6E, 0x0000736E}, -- شوێنەواری ئەتڵانتس
    {1634034218, 1601795189, 1769239137, 1902081139, 1953653109, 29285}, -- ناوچەی هونەری
    {1634486042, 1852403821, 1631805287, 28781, 120, 0},            -- واحەی شار
    {0x756C702C, 0x6E556873, 0x726F6369, 0x61765F6E, 0x746E656C, 0x00656E69}, -- تەنیای شاخدار
    {1852403222, 1801412970, 1701210478, 0, 0, 0},                  -- پادشای میوە
    {0x7361651A, 0x48726574, 0x6F6D6D61, 0x00006B63, 0, 0},          -- پشووی مانگا
    {1769302556, 1717527907, 1953396079, 7235937, 1886546241, 7631471}, -- فوارەی پرتەقاڵ
    {1952544548, 1852404325, 1851868007, 1935762783, 7497076, 0},      -- کەشتی چەتەکان
    {1819239208, 1866887791, 1635020405, 1834970729, 1751348321, 51},  -- خەڵاتە زەبەلاحەکە
    {1667580958, 1415541359, 1214604658, 1702065519, 0, 0},            -- فوارەی کارلێکەر
    {1634034212, 1601795189, 2003790950, 1985966693, 6648673, 118},    -- ڕەزی ترێ
    {1634034216, 1601795189, 1702125943, 1869438834, 1702130542, 114}, -- قۆچی پڕ بەرەکەت
    {1701860140, 1818323299, 1969317186, 1935636852, 1869111653, 6648690}, -- سروشتی دایک
    {0x6165622A, 0x5F797475, 0x74736165, 0x6C5F7265, 0x65746E61, 0xFF006E72}, -- پاشای دەریاکان
    {0x6570532C, 0x6C616963, 0x75616542, 0x665F7974, 0x6853796C, 0x00706565}, -- فڕینی تایبەت
    {0x6570532A, 0x6C616963, 0x75616542, 0x665F7974, 0x7544796C, 0x00646B63}, -- مراوی تایبەت
    {1768448786, 1751346019, 27497, 0, 0, 0}, -- کۆشکی زێڕین
    {1634034212, 1601795189, 1684955491, 1869111651, 6648693, 113}, -- باخچەی نهێنی
    {1684363038, 1735289188, 1147094067, 1919902565, 0, 0}, -- خانووی دار
    {1918984990, 1702065519, 1970429804, 1919250030, 0, 0}, -- دوولابی هەوا
    {1634034212, 1601795189, 1834973493, 1836412527, 7630437, 0}, -- خەڵاتی ٥ ساڵە
    {0x6E6F7022, 0x6F6D5F64, 0x72656874, 0x7261655F, 0x00006874, 0}, -- تەختی دایک
    {0x61747320, 0x5F657574, 0x74616F62, 0x6C6F675F, 0x656E0064, 0x00000072}, -- ئەسپە ئاوییەکە
    {0x6F6F7212, 0x6365645F, 0x0000726F, 0, 0, 0}, -- دیکۆری ڕۆژ
    {0x61656228, 0x5F797475, 0x676E756A, 0x745F656C, 0x6D65746F, 0x00000073}, -- تۆتمی دارستان
    {0x61656226, 0x5F797475, 0x676E756A, 0x725F656C, 0x736E6975, 0}, -- نیشانەی شاخ
    {0x61656226, 0x5F797475, 0x616C6F73, 0x79735F72, 0x6D657473, 0}, -- سیستەمی خۆر
    {0x61656216, 0x5F797475, 0x69746579, 0, 0, 0}, -- بوونەوەرە ئەفسانەییەکە
    {0x61656214, 0x5F797475, 0x006F6F66, 0, 0, 0}, -- شوێنی خۆراک
    {0x61656222, 0x5F797475, 0x6E697773, 0x61705F67, 0x00006D6C, 0}, -- جۆلانەی باخچە
    {0x6165621C, 0x5F797475, 0x6D6D616D, 0x0068746F, 0, 0}, -- مامۆس
    {0x6E6F6D1A, 0x7379656B, 0x616C705F, 0x00006B6E, 0, 0}, -- کلیلی پاشا
    {0x67695010, 0x6163734F, 0x61420072, 0x00000076, 0, 0}, -- بەرازی گۆشتخۆر
    {0x776F4312, 0x69747241, 0x62007473, 0x00000076, 0, 0}, -- مانگای هونەرمەند
    {0x706F7426, 0x79726169, 0x6D6F635F, 0x69746570, 0x6E6F6974, 0}, -- کۆمەڵەی ئاژەڵان
    {0x6C736918, 0x5F646E61, 0x66696E6B, 0x69000065, 0x6E6F6974, 0}, -- دوورگەی فینکی
    {0x6C615020, 0x65747465, 0x6C756353, 0x72757470, 0x61450065, 0x00000076}, -- پێڕەوی مەڕ
    {0x6E61631A, 0x725F7964, 0x626E6961, 0x6900776F, 0x6E6F6974, 0}, -- پەلکەزێڕینەی شەکر
    {0x72654D24, 0x44326567, 0x726F6365, 0x6F697461, 0x0030316E, 0x0034316E}, -- مێژووی شار
    {0x6F6C6618, 0x5F726577, 0x73756F68, 0x73720065, 0x006C6C00, 0}, -- خانووی گوڵەکان
    {1935762720, 1752327540, 1702065519, 1701999711, 808976485, 48}  -- کەشتی
}
local selectedDecoIndex = 0

-- ٢. فەنکشنی جوانکاری بە شێوازی مینۆ و قفلکراو
function Run_Decoration()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Deco_Menu_Loop()
        local names = {
            "الأحصنة الطائرة", "مركز المملكة", "لعبة على الماء", "عصارة العنب", 
"عصارة العنب 2", "تفاح الكراميل", "حبل الغسيل", "ديكور خاص", 
"النبات آكل اللحوم", "ركوب الدراجات", "أرجوحة الهوت دوغ", "قطار الحلويات", 
"شجرة الموز", "الأفضل على الإطلاق", "متجر الزهور", "كهف الراحة", 
"معرض الصور", "آثار أتلانتس", "المنطقة الفنية", "واحة المدينة", 
"الوحيد ذو القرون", "ملك الفاكهة", "استراحة البقرة", "نافورة البرتقال", 
"سفينة القراصنة", "الجائزة الضخمة", "النافورة التفاعلية", "مزرعة العنب", 
"قرن الوفرة", "الطبيعة الأم", "ملك البحار", "الطيران الخاص", 
"البطة الخاصة", "القصر الذهبي", "الحديقة السرية", "بيت الشجرة", 
"دولاب الهواء", "جائزة الـ 5 سنوات", "عرش الأم", "حصان البحر", 
"ديكور الشمس", "توتيم الغابة", "علامة الجبل", "النظام الشمسي", 
"المخلوق الأسطوري", "مكان الطعام", "أرجوحة الحديقة", "الماموث", 
"مفتاح الملك", "الخنزير آكل اللحوم", "البقرة الفنانة", "مجموعة الحيوانات", 
"جزيرة الفينيق", "مسار الأغنام", "قوس قزح السكري", "تاريخ المدينة", 
"بيت الزهور", "السفينة الهادئة"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedDecoIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "خروج 🔙")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then 
            return Deco_Menu_Loop() 
        end
        
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedDecoIndex = choice
        local codes = decoration_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Deco_Menu_Loop() 
    end

    Deco_Menu_Loop()
end


-- ١. لیستی کۆدی جوانکارییەکانی ئاو بە کوردی
local water_decoration_collection = {
    {1952536352, 1967288933, 1818322798, 1347647343, 1761280057, 0},    -- سەکۆی نیشتنەوە
    {1634292250, 1601139820, 1684632130, 25959, 1939298051, 116},       -- ڤێلای سەر ئاو
    {2036811040, 1632662640, 1970436464, 1634681459, -1609498508, 123}, -- پردی ڤینیسی
    {0x6C696626, 0x6B61696D, 0x5F676E69, 0x61657274, 0x65727573, 0},    -- بەلەمی میسری
    {0x69615328, 0x676E696C, 0x74666152, 0x6572745F, 0x72757361, 0x00000065}, -- جادوی سینەما
    {1634034218, 1601795189, 1634497633, 1936290926, 1953458271, 27749}, -- کەمپی سەر ئاو
    {1634486038, 1916957555, 1701274729, 0, 0, 0},                      -- شوێنی پشوو
    {0x61656228, 0x5F797475, 0x65746177, 0x6F6D5F72, 0x6574736E, 0x00000072}, -- دێوەزمەی نێس
    {0x61656228, 0x5F797475, 0x73756F68, 0x6C614D65, 0x65766964, 0x00000073}, -- خانووی بێنگالۆ
    {1634034210, 1601795189, 1634497633, 1634230131, 989881454, 111},   -- ڕمبەکەی ئەتڵانتس
    {1701860138, 1818323299, 1969317186, 1834973556, 1634562661, 25705}, -- پەری دەریا
    {1634034220, 1601795189, 1634888048, 1935631732, 1601202536, 7827298}, -- مەلەوانگەی شاهانە
    {1668440360, 1868915048, 2036821868, 1819566431, 1769238113, 115}, -- بەلەمی گەشتیاری
    {1634034220, 1601795189, 1836674127, 1180920176, 1953396079, 7235937}, -- فوارەی جیهانی
    {1634034220, 1601795189, 1650811753, 1600615013, 1735288176, 7235957}, -- باخچەی سەهۆڵی
    {1818322984, 1702326124, 1734307429, 1953722116, 1768452959, 112},  -- کەشتی جنۆکە
    {1634034212, 1601795189, 1752394086, 1918987615, 7628139, 0}, -- هێمای دەریا
    {1634034206, 1601795189, 1702063984, 1852793961, 0, 0}, -- بەلەمی خێرا
    {1634034212, 1601795189, 1702259044, 1650422642, 7627119, 121},     -- مەلەوانەکان
    {1634034216, 1601795189, 1668178275, 1751085669, 1768780389, 116},  -- قڕژاڵی گوشەگیر
    {1701860140, 1818323299, 1969317186, 1935636852, 1869111653, 6648690}, -- ئەسپە ئاوییەکە
    {0x61656222, 0x5F797475, 0x736F6867, 0x68735F74, 0x00007069, 0},    -- کەشتییە ترسناکەکە
    {1634034214, 1601795189, 1684955491, 1919049593, 1701274729, 0},    -- پردی شیرینی
    {0x69616616, 0x775F7972, 0x72657461, 0, 0, 0}                       -- جنۆکەی ئاو
}

local selectedWaterIndex = 0

-- ٢. فەنکشنی جوانکارییەکان بە شێوازی مینۆ و قفلکراو
function Run_Water_Decoration()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Water_Menu_Loop()
        local names = {
           "منصة الهبوط", "فيلا فوق الماء", "الجسر الفينيسي", "القارب المصري", 
"سحر السينما", "التخييم على الماء", "مكان الاستراحة", "وحش نيس", 
"منزل البنغالو", "رمح أتلانتس", "حورية البحر", "المسبح الملكي", 
"قارب الرحلات", "النافورة العالمية", "الحديقة الجليدية", "سفينة الأشباح", 
"رمز البحر", "القارب السريع", "السباحون", "السلطعون الناسك", 
"حصان البحر", "السفينة المرعبة", "جسر الحلويات", "شبح الماء"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedWaterIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "خروج 🔙")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        -- قفڵکردنی مینۆکە
        if choice == nil then 
            return Water_Menu_Loop() 
        end
        
        -- گەڕانەوە بۆ مینۆی سەرەکی
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedWaterIndex = choice
        local codes = water_decoration_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Water_Menu_Loop() 
    end

    Water_Menu_Loop()
end

-- ١. لیستی کۆدی نافوورەکان بە کوردی
local fountain_collection = {
    {1767982620, 1180662130, 1953396079, 7235937, 672503271, 110},   -- نافوورەی پەری گوڵاوی
    {1634034216, 1601795189, 1769369421, 1970226789, 1767994478, 110}, -- نافوورەی فیلم
    {0x6E6F701C, 0x69775F64, 0x635F6874, 0x00707261, 0, 0},            -- نافوورەی نەهەنگ ١
    {1936291606, 1735289192, 1819043159, 0, 0, 0},                     -- دەریاچەی نێرگز ١
    {1684369946, 1768712524, 1867543397, 25710, 0, 0},                 -- دەریاچەی نێرگز ٢
    {1634034208, 1601795189, 1885695077, 1953390952, 67305587, 0},     -- فیلە دڵخۆشەکان
    {1801546788, 1970235493, 1650419059, 1953784175, 7367026, 113},    -- نافوورەی ڕووناکی
    {0x6172431A, 0x6F46656E, 0x61746E75, 0x00006E69, 0x92801DDB, 0x7B}, -- نافوورەی جادوویی
    {1935762710, 1601332596, 1684959088, 0, 0, 0},                     -- یاری بەلەم سواری
    {0x6E6F701C, 0x69775F64, 0x635F6874, 0x00707261, 0, 0},            -- فوارەی دڵخۆشی
    {0x756F661C, 0x6961746E, 0x68775F6E, 0x00656C61, 0x34FF9DF0, 0x72}, -- نافوورەی نەهەنگ ٢
    {1852796962, 1869438820, 1919248500, 1918985567, 1912629364, 116}, -- دەریاچەی سروشتی دایک
    {1852796956, 1769430884, 1667197044, 7369313, 0, 0},               -- گۆمە ماسی فرح
    {1935754526, 1601332596, 1853189990, 1852399988, 3690496, 27491}   -- نافوورەی جەژنی قیامەت
}

local selectedFountainIndex = 0

-- ٢. فەنکشنی نافوورەکان بە شێوازی مینۆ و قفلکراو
function Run_Fountain()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Fountain_Menu_Loop()
        local names = {
            "نافورة جنيّة الزهور", "نافورة الأفلام", "نافورة الحوت 1", 
"بحيرة النرجس 1", "بحيرة النرجس 2", "الفيلة السعيدة", 
"نافورة الضياء", "النافورة السحرية", "لعبة ركوب القوارب", 
"نافورة البهجة", "نافورة الحوت 2", "بحيرة الطبيعة الأم", 
"بركة أسماك الفرح", "نافورة العيد"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedFountainIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "خروج 🔙")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        -- قفڵکردنی مینۆکە
        if choice == nil then 
            return Fountain_Menu_Loop() 
        end
        
        -- گەڕانەوە بۆ مینۆی سەرەکی
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedFountainIndex = choice
        local codes = fountain_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Fountain_Menu_Loop() 
    end

    Fountain_Menu_Loop()
end

-- ١. لیستی کۆدی ماڵی ساحیرەکان بە کوردی
local witch_house_collection = {
    {1818322974, 1702326124, 2002742885, 1751348329, 642231808, 114}, -- ساحیرە و دەرمان
    {1836404762, 1852402544, 1970227295, 25971, 0, 0},                -- کێڵگەی کولەکە
    {1701988134, 1869114981, 1600484213, 1684370000, 1919906913, 0},  -- موشەکەکان
    {1886930220, 1953064037, 1148088169, 1919902565, 1869182049, 3289710}, -- ئاشەبا
    {1818322984, 1702326124, 1734307429, 1953722216, 1768452959, 112}, -- کەشتی جنۆکە
    {0x6C616820, 0x65776F6C, 0x6D5F6E65, 0x75657375, 0x68A2006D, 0},   -- ژووری نەفرەتلێکراو
    {1634488340, 1398762350, 7368552, 0, 0, 0},                        -- قوتابخانەی سیحر
    {0x61686322, 0x7265626D, 0x6C61685F, 0x65776F6C, 0x00006E65, 0},   -- ماڵی ترس
    {0x6C61481C, 0x65776F6C, 0x505F6E65, 0x006B7261, 0, 0},            -- کۆشکی شەڕانگێز
    {0x6C61682A, 0x65776F6C, 0x735F6E65, 0x6F637261, 0x67616870, 0x7375}, -- تابووتی بەردین
    {0x6F68671E, 0x796C7473, 0x72726143, 0x65676169, 0, 0},            -- گالیسکەی ترس
    {0x616C501C, 0x575F6B6E, 0x77657265, 0x00666C6F, 0, 0},            -- شانۆی گورگینە
    {0x746F4718, 0x5F636968, 0x65776F54, 0x72, 0, 0},                  -- بورجی تۆقێنەر
    {0x6D75501A, 0x6E696B70, 0x74654D5F, 0x72, 0, 0},                  -- ڕێڕەوی نهێنی
    {0x6C616824, 0x65776F6C, 0x675F6E65, 0x6F677261, 0x00656C79, 0},   -- شەمشەمەکوێرەکان
    {0x6C616820, 0x65776F6C, 0x635F6E65, 0x6C747361, 0x65, 0},         -- قەڵای تاریکی
    {0x6C616828, 0x65776F6C, 0x775F6E65, 0x68637469, 0x7269685F, 0x65}, -- پارکی ساحیرەکان
    {0x6C616824, 0x65776F6C, 0x665F6E65, 0x746E756F, 0x61, 0},         -- فوارەی شوم
    {0x6C616826, 0x65776F6C, 0x735F6E65, 0x65726163, 0x776F7263, 0},   -- داوەڵەی کولەکە
    {0x6C61681C, 0x65776F6C, 0x705F6E65, 0x00706D75, 0, 0},            -- پیاوی کولەکە
    {0x6C61681E, 0x65776F6C, 0x775F6E65, 0x68637469, 0, 0},            -- ساحیرە و مەنجەڵ
    {0x74695710, 0x6F506863, 0x74, 0, 0, 0},                           -- مەنجەڵی سیحر
    {0x6C61681A, 0x65776F6C, 0x635F6E65, 0x7461, 0, 0},                -- پشیلە ڕەشەکە
    {1818314782, 1702326124, 1331654245, 1851877234, 672503040, 110},  -- نمایشی ترسناک
    {1818314780, 1702326124, 1348431461, 7041633, 672503271, 110},     -- قەسرە شوومەکە
    {1634027554, 1936026724, 1867014003, 1835365234, 671116897, 110},  -- سوارچاکی کولەکە
    {1634488340, 1398762350, 7368552, 110, 672503271, 110},            -- فرۆشگای ساحیرە
    {1953449752, 1600350568, 1702326100, 114, 672503271, 110},         -- بورجی مەرگ
    {1836404762, 1852402544, 1970227295, 25971, 672503271, 110}        -- ماڵی ساحیرە
}

local selectedWitchIndex = 0

-- ٢. فەنکشنی ماڵی ساحیرەکان بە شێوازی مینۆ و قفلکراو
function Run_Witch_Houses()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Witch_Menu_Loop()
        local names = {
         "الساحرة والجرعة", "مزرعة اليقطين", "الصواريخ", "طاحونة الهواء", 
"سفينة الأشباح", "الغرفة الملعونة", "مدرسة السحر", "بيت الرعب", 
"القصر الشرير", "التابوت الحجري", "عربة الرعب", "مسرح المستذئب", 
"البرج المرعب", "الممر السري", "الخفافيش", "قلعة الظلام", 
"حديقة الساحرات", "النافورة المشؤومة", "فزاعة اليقطين", "رجل اليقطين", 
"الساحرة والمرجل", "مرجل السحر", "القط الأسود", "العرض المرعب", 
"القصر المشؤوم", "فارس اليقطين", "متجر الساحرة", "برج الموت", 
"بيت الساحرة"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedWitchIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "خروج 🔙")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then 
            return Witch_Menu_Loop() 
        end
        
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedWitchIndex = choice
        local codes = witch_house_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Witch_Menu_Loop() 
    end

    Witch_Menu_Loop()
end

-- ١. لیستی کۆدی دارەکان بە کوردی
local trees_collection = {
    {1701999640, 1752391525, 1852403809, 103, 0, 0},                  -- داری سەبەتەی فرح
    {0x61656222, 0x5F797475, 0x646E6163, 0x72745F79, 0x6565, 0},      -- داری میوە
    {1634034212, 1601795189, 1735292266, 1834968428, 7040623, 0},     -- داری مۆز
    {0x736E6920, 0x6C6C6174, 0x6F697461, 0x72615F6E, 0xC8770074, 0x71}, -- داری سەرسوڕهێنەر
    {0x6F6F621E, 0x6572546B, 0x756A5F65, 0x656C676E, 0, 0},            -- داری جەنگەڵ
    {0x6968431A, 0x6573656E, 0x7254594E, 0x6565, 0, 0},                -- داری گڵۆپدار
    {0x6B616A12, 0x6E617261, 0xF3006164, 0x068CC6A3, 0xAD5C4DF0, 0x7A}, -- داری جاکاراندا
    {1634034208, 1601795189, 1701734768, 1701999711, 101, 0},         -- داری سنەوبەر
    {1634034208, 1601795189, 1734439521, 1701732725, 121, 0},         -- داری مۆر
    {1634034204, 1601795189, 1869374820, 7891310, 0, 0},               -- داری پۆنسیمانا
    {1634034206, 1601795189, 1953720695, 1634300517, 0, 0},            -- داری ویستریا
    {1634034214, 1601795189, 1685022834, 1852138607, 1852797540, 0},  -- داری گوڵەباخ
    {1634034212, 1601795189, 1701147252, 1818321503, 7237484, 121},    -- داری فووکردن (نەرم)
    {0x7265621E, 0x72547972, 0x6B5F6565, 0x6566696E, 0, 0}             -- داری توو
}

local selectedTreeIndex = 0

-- ٢. فەنکشنی دارەکان بە شێوازی مێنۆ و قفلکراو
function Run_Trees()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Trees_Menu_Loop()
        local names = {
            "شجرة سلة الفرح", "شجرة الفاكهة", "شجرة الموز", "الشجرة المذهلة", 
"شجرة الغابة", "الشجرة المضيئة", "شجرة الجاكاراندا", "شجرة الصنوبر", 
"شجرة الأرجوان", "شجرة البونسيانا", "شجرة الويستريا", "شجرة الورد", 
"شجرة النفخ", "شجرة التوت"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedTreeIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then 
            return Trees_Menu_Loop() 
        end
        
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedTreeIndex = choice
        local codes = trees_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Trees_Menu_Loop() 
    end

    Trees_Menu_Loop()
end

-- ١. لیستی کۆدی کەروێشکەکان بە کوردی
local rabbit_collection = {
    {1819230994, 1163883119, 671115111, 110, 672503271, 110},         -- فرۆشگای جەژنی پەنیر
    {0x7361451C, 0x5F726574, 0x6E6E7562, 0x00736569, 0, 0},            -- پارکی کەروێشکەکان
    {1935762716, 1383228788, 1919707489, 6578543, 73836291, 0},        -- هێڵی ئاسنی ئیستەر
    {1935762716, 1601332596, 1952670054, 7959151, 0, 0},               -- وۆرک شۆپی ئیستەر
    {1935754526, 846357876, 114, 4467760, 1919902565, 0},              -- گوندی کەروێشکەکان
    {1935754518, 1400006004, 1886221684, 0, 0, 0},                     -- ماڵی کەروێشکەکان ١
    {1935754524, 1601332596, 1852732770, 7562601, 0, 0},               -- گەنجینەی کەروێشک
    {1734435362, 1852732786, 1600613993, 1953718629, 1627419237, 25972} -- پێشبڕکێی ڕاکردن
}

local selectedRabbitIndex = 0

-- ٢. فەنکشنی کەروێشکەکان بە شێوازی مێنۆ و قفلکراو
function Run_Rabbit_Houses()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Rabbit_Menu_Loop()
        local names = {
            "متجر مهرجان الجبن", "حديقة الأرانب", "سكك حديد عيد الفصح", 
"ورشة عمل عيد الفصح", "قرية الأرانب", "بيت الأرانب 1", 
"كنز الأرنب", "سباق الجري"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedRabbitIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then 
            return Rabbit_Menu_Loop() 
        end
        
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedRabbitIndex = choice
        local codes = rabbit_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Rabbit_Menu_Loop() 
    end

    Rabbit_Menu_Loop()
end

-- ١. لیستی کۆدی سیاج و بەربەستەکان بە کوردی
local fence_collection = {
    {1634034214, 1601795189, 2003790918, 1734308453, 1936028769, 0},   -- دەروازەی گوڵەکان
    {1634034214, 1601795189, 1970828620, 1734310258, 1936028769, 0},   -- دەروازەی شکۆمەندی
    {1768440602, 1702061422, 1852139103, 25955, 0, 0},                -- سیاجی ڕۆژهەڵاتی
    {1919435550, 1836348265, 1717531489, 1701015141, 0, 0},            -- سیاجی سەری ساڵ
    {1851876118, 1717533028, 1701015141, 0, 0, 0},                    -- سیاجی زەنجەبیلی
    {0x6165531C, 0x636E6546, 0x65665F65, 0x0065636E, 0, 0},            -- سیاجی دەریایی
    {1819558172, 1769238113, 1701207923, 6644590, 0, 0},               -- سیاجی مەرجانی
    {1818318370, 1769238117, 1415538030, 1634300015, 31090, 0},        -- پەیکەری خۆشەویستی
    {2003127824, 1634031967, 114, 0, 0, 0},                            -- بیست و دوو
    {1935754520, 1601332596, 1668179302, 101, 0, 0},                   -- سیاجی جەژنی ئیستەر
    {1818318380, 1769238117, 1751082350, 1953653093, 1632136777, 7562350}, -- خۆشەویستی هەمیشەیی
    {1851876116, 1734310244, 6648929, 113, 0, 0},                      -- دەروازەی زەنجەبیلی
    {0x65687316, 0x64657261, 0x65657254, 0, 0, 0},                     -- داری سێبەر
    {0x6E6F701C, 0x69775F64, 0x635F6874, 0x00707261, 0, 0},            -- حەوزی ماسی
    {1634034206, 1601795189, 1215917158, 1702065519, 0, 113},          -- ماڵی باڵندە
    {0x72696420, 0x61656769, 0x73656C62, 0x75746174, 0x656E0065, 0x72}, -- باڵۆنی بەرازی
    {0x63656D18, 0x72745368, 0x616D7761, 0x6E, 0xC9D85C63, 0x71},      -- داوەڵەی میکانیکی
    {1634034206, 1601795189, 1633836851, 1852796012, 0, 0},            -- ژمارە سێ
    {1919435554, 1836348265, 1818194785, 1702129249, 67137138, 113},   -- ستوونی ڕووناکی
    {1650551840, 1852404345, 1700751476, 1702130529, 114, 0},          -- مەزەی ئیستەر
    {1818318380, 1769238117, 1885300078, 1868916585, 1818194798, 6649455}, -- کۆتری عاشقان
    {1635021594, 1600484724, 1953067639, 29285, 0, 0},                 -- نووسەری یەکەم
    {2020961304, 1601794677, 1668179302, 101, 0, 0}                    -- سیاجی زێڕین
}

local selectedFenceIndex = 0

-- ٢. فەنکشنی سیاجەکان بە شێوازی مێنۆ و قفلکراو
function Run_Fences()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        return gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})

    local function Fence_Menu_Loop()
        local names = {
           "بوابة الزهور", "بوابة المجد", "السياج الشرقي", "سياج رأس السنة", 
"سياج الزنجبيل", "السياج البحري", "السياج المرجاني", "تمثال الحب", 
"اثنان وعشرون", "سياج عيد الفصح", "الحب الأبدي", "بوابة الزنجبيل", 
"شجرة الظل", "بركة الأسماك", "بيت الطيور", "منطاد الخنزير", 
"الفزاعة الميكانيكية", "رقم ثلاثة", "عمود الضياء", "متاهة عيد الفصح", 
"حمامة العشاق", "الكاتب الأول", "السياج الذهبي"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedFenceIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then 
            return Fence_Menu_Loop() 
        end
        
        if choice == #displayNames then 
            Main_Menu() 
            return 
        end

        selectedFenceIndex = choice
        local codes = fence_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        
        return Fence_Menu_Loop() 
    end

    Fence_Menu_Loop()
end
 
-- ==========================================
-- SEROK ARAM LUXURY - بەشی ئاژەڵەکان
-- ==========================================
-- ١. لیستی مریشکەکان بە کوردی
local chickens_collection = {
    {1768641324, 1749245806, 1701536617, 1634033518, 1919251571, 3290975}, -- مریشکی جەژنی ئیستەر
    {1768641318, 1749245806, 1701536617, 1850433390, 1952999273, 0},       -- مریشکی سوارچاک
    {1768641322, 1749245806, 1701536617, 1634557806, 808612722, 13618},    -- مریشکی بۆشایی ئاسمان
    {1768641320, 1749245806, 1701536617, 1852006254, 842019449, 53},       -- مریشکی ئاهەنگگێڕ
    {1768641318, 1749245806, 1701536617, 1701338990, 1935764588, 0},       -- مریشکی پەری
    {1768641320, 1749245806, 1701536617, 1919508334, 1851878501, 100},     -- مریشکی سەری ساڵ
    {1768641316, 1749245806, 1701536617, 2004049774, 7628133, 0},          -- مریشکی گەڕیدە
    {1768641318, 1749245806, 1701536617, 1969905518, 1701603182, 0},       -- مریشکی هاندەر
    {1768641316, 1749245806, 1701536617, 1886609262, 7631471, 0},          -- مریشکی فڕۆکەوان
    {1768641318, 1749245806, 1701536617, 1920229230, 1818588769, 0}        -- مریشکی هاندەر ٢
}

local selectedChickenIndex = 0

-- ٢. مێنۆی سەرەکی ئاژەڵەکان بە نیشانەی دەستنیشانکردن (Checkbox)
function Run_Animals_Menu()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🐔            اكواد دجاح                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🐄          حظيرة أبقار                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🐏           اكواد خراف                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🐖           اكواد الخنازير              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄           رجـــــــــــــوع                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪           خـــــــــــــروج                 ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

if menu == nil then 
    gg.setVisible(false) -- مێنووەکە دەشارێتەوە
    
    -- ئەم بەشە سکرێپتەکە دەخەوێنێت هەتا خۆت کلیک لە گەیم جاردن دەکەیتەوە
    while true do
        if gg.isVisible() then
            gg.setVisible(false)
            return Run_Animals_Menu() -- کاتێک خۆت کلیکت کردەوە، ئینجا مێنووەکە پیشان دەدات
        end
        gg.sleep(100) -- بۆ ئەوەی لۆد لەسەر مۆبایلەکە دروست نەبێت
    end
end

    -- لێرە پشکنین دەکەین کامەی تحدید کراوە
    if menu[1] then Run_Chickens() end
    if menu[2] then Run_Cows() end
    if menu[3] then Run_Sheeps() end
    if menu[4] then Run_Pigs() end
    
    if menu[5] then 
        if PdaistakanyYari then PdaistakanyYari() end
        return 
    end
    if menu[6] then os.exit() end
end

-- ٣. فەنکشنی مریشکەکان بە مێنۆی هەڵبژاردن (Radio Style)
function Run_Chickens()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local r = gg.getResults(1)
    
    if #r == 0 then 
        gg.setVisible(true)
        gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن  ") 
        return Run_Animals_Menu() 
    end
    
    local cell3 = r[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Chicken_Selection_Loop()
        local names = {
            "دجاجة عيد الفصح", "الدجاجة الفارس", "دجاجة الفضاء", 
"الدجاجة المحتفلة", "الدجاجة الجنية", "دجاجة رأس السنة", 
"الدجاجة المستكشفة", "الدجاجة المشجعة", "الدجاجة الطيار", "الدجاجة المشجعة 2"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedChickenIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then return Chicken_Selection_Loop() end
        if choice == #displayNames then 
            -- لادانی فریز پێش گەڕانەوە بۆ مێنۆی ئاژەڵەکان
            gg.removeListItems(gg.getListItems())
            return Run_Animals_Menu() 
        end

        selectedChickenIndex = choice
        local codes = chickens_collection[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Chicken_Selection_Loop()
    end

    Chicken_Selection_Loop()
end


-- ١. لیستی مانگاکان بە کوردی
local cow_list = {
    {1768641320, 1866686318, 1633902455, 1986621042, 929000545, 48}, -- مانگای کەرنەڤاڵ
    {1768641304, 1866686318, 1313038199, 89, 0, 0},                 -- مانگای ئاهەنگگێڕ
    {1768641316, 1866686318, 1919311735, 1701015137, 3683935, 0},   -- مانگای فەرەنسی
    {1768641324, 1866686318, 1765957495, 1684567154, 845117793, 3486256}, -- مانگای چاویلکە لەچاو
    {1768641308, 1866686318, 1634361207, 7233904, 0, 0},            -- مانگای یابانی
    {1768641306, 1866686318, 1918984055, 25185, 0, 0},              -- مانگای عەرەبی
    {1768641314, 1866686318, 1701207927, 1986622579, 27745, 0},     -- مانگای گوڵەکان
    {1768641306, 1866686318, 1634557815, 29554, 0, 0},              -- مانگای کەشتیوان
    {1768641322, 1866686318, 1818451831, 1769173857, 1937075555, 25449}, -- مانگای سيمفۆنی
    {1768641318, 1866686318, 1634033527, 1919251571, 875704370, 0}, -- مانگای ئیستەر
    {1768641310, 1866686318, 1918984055, 1667855459, 0, 0},         -- مانگای جەمسەری
    {1768641318, 1866686318, 1768972151, 1702125938, 875704370, 0}, -- مانگای چەتەکان
    {1768641322, 1866686318, 1768054647, 1684567154, 808614241, 13362}, -- مانگای ئاهەنگگێڕ ٢
    {1768641316, 1866686318, 1953062775, 846818401, 3420720, 0},    -- مانگای شیک
    {1768641314, 1866686318, 1952538487, 1953390956, 29545, 0},     -- شاژنی ئەتڵەنتس
    {1768641320, 1866686318, 1769430903, 1919251566, 1919905875, 116}, -- مانگای کێوی
    {1768641324, 1866686318, 1634230135, 2003790956, 846095717, 3355184}, -- مانگای نۆسفراتۆ
    {1768641310, 1866686318, 2004049783, 846488933, 0, 0},          -- مانگای شیرینی دروستکەر
    {1768641308, 1866686318, 2004049783, 7628133, 0, 0},            -- مانگای سەری ساڵ
    {1768641314, 1866686318, 1768054647, 1684567154, 31073, 0},     -- مانگای ڤیستیڤاڵ
    {1768641316, 1866686318, 1635147639, 1953391980, 6647401, 0},   -- مانگای نازدار
    {1768641324, 1866686318, 1751342967, 1953720690, 846422381, 3289648}, -- مانگای کورتەباڵا
    {1768641308, 1866686318, 1869438839, 6646134, 0, 0}             -- مانگای سینەمایی
}

local selectedCowIndex = 0

-- ٢. فەنکشنی مانگاکان بە مێنۆی هەڵبژاردنی بازنەیی
function Run_Cows()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Animals_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Cow_Selection_Loop()
        local names = {
            "بقرة الكرنفال", "البقرة المحتفلة", "البقرة الفرنسية", "البقرة ذات النظارات", 
"البقرة اليابانية", "البقرة العربية", "بقرة الزهور", "البقرة البحارة", 
"البقرة السمفونية", "بقرة عيد الفصح", "البقرة القطبية", "بقرة القراصنة", 
"البقرة المحتفلة 2", "البقرة الأنيقة", "ملكة أتلانتس", "البقرة البرية", 
"بقرة نوسفراتو", "البقرة صانعة الحلويات", "بقرة رأس السنة", 
"بقرة المهرجان", "البقرة اللطيفة", "البقرة القزمة", "البقرة السينمائية"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedCowIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then return Cow_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Animals_Menu() 
        end

        selectedCowIndex = choice
        local codes = cow_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Cow_Selection_Loop()
    end

    Cow_Selection_Loop()
end

-- ١. لیستی مەڕەکان بە کوردی
local sheep_list = {
    {1768641314, 1750294382, 1601201509, 1937006919, 31074, 0},      -- مەڕی گاتسبی
    {1768641322, 1750294382, 1601201509, 1819043176, 808612705, 13618}, -- مەڕی ئەفسانەیی
    {1768641322, 1750294382, 1601201509, 1903386989, 1634887029, 25956}, -- مەڕی سەماکەر (هۆڵ)
    {1768641312, 1750294382, 1601201509, 1887004517, 116, 0},      -- مەڕی میسری
    {1768641314, 1750294382, 1601201509, 1734962795, 29800, 0},      -- مەڕی جەنگاوەر
    {1768641314, 1750294382, 1601201509, 2053206626, 27753, 0},      -- مەڕی سامبا
    {1768641320, 1750294382, 1601201509, 1768058738, 1869564014, 100}, -- مەڕی دزە ڕەسەنەکە
    {1768641312, 1750294382, 1601201509, 1701148531, 116, 0},      -- مەڕی سەری ساڵ
    {1768641320, 1750294382, 1601201509, 1702126948, 1986622563, 101}, -- مەڕی لێکۆڵەر
    {1768641320, 1750294382, 1601201509, 1685221230, 1866949481, 100}, -- مەڕی جەمسەری
    {1768641322, 1750294382, 1601201509, 1953718629, 808612453, 13106}, -- مەڕی جەژنی ئیستەر
    {1768641324, 1750294382, 1601201509, 1634628972, 844713586, 3289648} -- مەڕی فێستیڤاڵی بەهار
}

local selectedSheepIndex = 0

-- ٢. فەنکشنی مەڕەکان بە مێنۆی هەڵبژاردن
function Run_Sheeps()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Animals_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Sheep_Selection_Loop()
        local names = {
            "خروف غاتسبي", "الخروف الأسطوري", "الخروف الراقص", "الخروف المصري", 
"الخروف المحارب", "خروف السامبا", "الخروف اللص الأصلي", "خروف رأس السنة", 
"الخروف المحقق", "الخروف القطبي", "خروف عيد الفصح", "خروف مهرجان الربيع"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedSheepIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")       

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then return Sheep_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Animals_Menu() 
        end

        selectedSheepIndex = choice
        local codes = sheep_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Sheep_Selection_Loop()
    end

    Sheep_Selection_Loop()
end


-- ١. لیستی بەرازەکان بە کوردی
local pig_list = {
    {1768641304, 1766874990, 1313038183, 89, 0, 0},         -- بەرازی ئاهەنگگێڕ
    {1768641324, 1766874990, 1635147623, 1953391980, 1936027241, 7954756} -- بەرازی کیوبید (دڵداری)
}

local selectedPigIndex = 0

-- ٢. فەنکشنی بەرازەکان بە مێنۆی هەڵبژاردن
function Run_Pigs()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Animals_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Pig_Selection_Loop()
        local names = {
           "الخنزير المحتفل", 
"خنزير كيوبيد (الحب)"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedPigIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋\n╚══════════════════════╝")

        if choice == nil then return Pig_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Animals_Menu() 
        end

        selectedPigIndex = choice
        local codes = pig_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Pig_Selection_Loop()
    end

    Pig_Selection_Loop()
end



-- ==========================================
-- SEROK ARAM - بەشی جوانکاری وێزگەکان
-- ==========================================
-- ١. لیستی شەمەندەفەرەکان بە کوردی
local train_list = {
    {1768641308, 1918132078, 1601071457, 3297363, 0, 0},         -- شەمەندەفەری پاشەڕۆژ
    {1768641320, 1918132078, 1601071457, 1851880038, 912221539, 56}, -- شەمەندەفەری فەڕەنسی
    {1768641322, 1918132078, 1601071457, 1819043176, 808612705, 13618}, -- شەمەندەفەری ئەفسانەیی
    {1768641318, 1918132078, 1601071457, 1953719654, 1818326633, 0}, -- شەمەندەفەری گوڵەکان
    {1768641322, 1918132078, 1601071457, 1634035828, 1667854964, 27745}, -- شەمەندەفەری شانۆیی
    {1768641324, 1918132078, 1601071457, 1751478896, 1869902697, 6515058}, -- شەمەندەفەری سەرەتایی
    {1768641314, 1918132078, 1601071457, 1953718629, 29285, 0},      -- شەمەندەفەری جەژنی ئیستەر
    {1768641320, 1918132078, 1601071457, 1768058738, 1869564014, 100}, -- عارەبانەی دارین
    {1768641320, 1918132078, 1601071457, 1769105507, 1634563187, 115}, -- شەمەندەفەری سەری ساڵ
    {1768641314, 1918132078, 1601071457, 1734962795, 29800, 0},      -- شەمەندەفەری سوارچاکەکان
    {1768641324, 1918132078, 1601071457, 1634628972, 844713586, 3289648}, -- شەمەندەفەری ئەژدیهاکان
    {1768641310, 1918132078, 1601071457, 1936875885, 0, 0},          -- شەمەندەفەری مەریخ
    {1768641316, 1918132078, 1601071457, 1953719671, 7238245, 0},    -- شەمەندەفەری ڕاوچییەکان
    {1768641322, 1918132078, 1399744865, 1769234804, 1398763119, 14416}, -- وێستگەی دیسکۆ
    {1768641308, 1918132078, 1601071457, 3493971, 0, 0},             -- شەمەندەفەری مۆتەکە
    {1768641312, 1918132078, 1601071457, 976375891, 50, 0}           -- شەمەندەفەری خێرا
}

local selectedTrainIndex = 0

-- ٢. مینۆی سەرەکی وێزگەکان (بە شێوازی Checkbox وەک وێنەکە)
function Run_Stations_Menu()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🚂           اكواد القطار               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚉         المحطة القيطار           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚁         اكواد هليكوبتر              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ✈️           اكواد الطائره              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🛳️           اكواد الميناء              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄           رجـــــــــــوع                   ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪            خــــــــروج                   ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return end

    if menu[1] then Run_Train_Logic() end
    if menu[2] then Run_Train_Station() end
    if menu[3] then Run_Helicopter() end
    if menu[4] then Run_Air_Mixed() end
    if menu[5] then Run_Ship_Island_Mixed() end
    
    if menu[6] then 
        if PdaistakanyYari then PdaistakanyYari() end
        return 
    end
    if menu[7] then os.exit() end
end

-- ٣. فەنکشنی شەمەندەفەرەکان
function Run_Train_Logic()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Stations_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Train_Selection_Loop()
        local names = {
            "قطار المستقبل", "القطار الفرنسي", "القطار الأسطوري", 
"قطار الزهور", "القطار المسرحي", "القطار البدائي", 
"قطار عيد الفصح", "العربة الخشبية", "قطار رأس السنة", 
"قطار الفرسان", "قطار التنانين", "قطار المريخ", 
"قطار الصيادين", "محطة الديسكو", "قطار الكابوس", "القطار السريع"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedTrainIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

        if choice == nil then return Train_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Stations_Menu() 
        end

        selectedTrainIndex = choice
        local codes = train_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Train_Selection_Loop()
    end

    Train_Selection_Loop()
end

-- ١. لیستی وێستگەکانی شەمەندەفەر بە کوردی
local trainstation_list = {
    {1768641322, 1918132078, 1399744865, 1769234804, 1398763119, 12880}, -- دەروازەی شەمەندەفەری خێرا
    {1768641324, 1918132078, 1399744865, 1769234804, 1834970735, 7565921}, -- وێستگەی هەسارەی مەریخ
    {1768641308, 1918132078, 1601071457, 3690579, 0, 0},                 -- وێستگەی دیسکۆ
    {1768641322, 1918132078, 1399744865, 1769234804, 1398763119, 13648}  -- وێستگەی مۆتەکە (ئەشباح)
}

local selectedStationIndex = 0

-- ٢. فەنکشنی وێستگەی شەمەندەفەر بە مێنۆی هەڵبژاردن
function Run_Train_Station()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Stations_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Station_Selection_Loop()
        local names = {
            "بوابة القطار السريع", 
"محطة كوكب المريخ", 
"محطة الديسكو", 
"محطة الكابوس"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedStationIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

        if choice == nil then return Station_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Stations_Menu() 
        end

        selectedStationIndex = choice
        local codes = trainstation_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Station_Selection_Loop()
    end

    Station_Selection_Loop()
end

-- ١. لیستی هەلیکۆپتەرەکان بە کوردی
local heli_list = {
    {1768641322, 1699241838, 1868786028, 1919251568, 1651462751, 29807}, -- گەیەنەری ئۆتۆماتیکی
    {1768641324, 1699241838, 1868786028, 1919251568, 1952532319, 7955059}, -- هەلیکۆپتەری تایبەت
    {1768641324, 1699241838, 1868786028, 1919251568, 1936020063, 7631471}, -- قەنەفەی فڕیو
    {1768641324, 1699241838, 1868786028, 1919251568, 1634882655, 7103862}, -- پاپۆڕی فڕیو
    {1768641324, 1699241838, 1868786028, 1919251568, 1634877791, 6515042}, -- فەرشی فڕیو
    {1768641322, 1699241838, 1868786028, 1919251568, 1868977503, 12858}, -- قاپە فڕیوە توربۆکە
    {1768641324, 1699241838, 1868786028, 1919251568, 1634886239, 7104890}, -- هەلیکۆپتەری پەڕەداری
    {1768641322, 1699241838, 1868786028, 1919251568, 1869632351, 29810}  -- بایسکیلە فڕیوەکە
}

local selectedHeliIndex = 0

-- ٢. فەنکشنی هەلیکۆپتەر بە مێنۆی هەڵبژاردن
function Run_Helicopter()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Stations_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Heli_Selection_Loop()
        local names = {
            "الناقل الآلي", "المروحية الخاصة", "الأريكة الطائرة", 
"السفينة الطائرة", "البساط الطائر", "الطبق الطائر التوربو", 
"المروحية ذات الشفرات", "الدراجة الطائرة"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedHeliIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

        if choice == nil then return Heli_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Stations_Menu() 
        end

        selectedHeliIndex = choice
        local codes = heli_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Heli_Selection_Loop()
    end

    Heli_Selection_Loop()
end

-- ١. لیستی تەیارەکان و فڕۆکەخانە بە کوردی
local air_mix_list = {
    {1768641314, 1765891950, 1634496626, 1935631726, 31088, 0},      -- تەیارەی مۆتەکە (Ghost)
    {1768641318, 1765891950, 1634496626, 1834968430, 1701410415, 0}, -- تەیارەی ئەستێرەکان
    {1768641316, 1765891950, 1634496626, 1918854510, 7037807, 0},    -- تەیارەی ڕۆک
    {1768641318, 1765891950, 1634496626, 1398760814, 842676048, 0},  -- ئەژدیهای ناوازە
    {1768641314, 1765891950, 1634496626, 1398760814, 14672, 0},      -- تەیارەی کەمەرەیی
    {1768641312, 1765891950, 1919905906, 1886609268, 121, 0},         -- فڕۆکەخانەی بنکەی نهێنی
    {1768641316, 1765891950, 1919905906, 1869438836, 6646134, 0},    -- فڕۆکەخانەی سینەمایی
    {1768641314, 1765891950, 1919905906, 1869766516, 27491, 0},      -- فڕۆکەخانەی ڕۆک
    {1768641312, 1765891950, 1919905906, 1347641204, 55, 0},         -- فڕۆکەخانەی فێستیڤاڵ
    {1768641320, 1765891950, 1919905906, 1634099060, 1869178995, 110} -- فڕۆکەخانەی مۆدێل
}

local selectedAirIndex = 0

-- ٢. فەنکشنی تەیارەکان بە مێنۆی هەڵبژاردن
function Run_Air_Mixed()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن  ") 
        return Run_Stations_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Air_Selection_Loop()
        local names = {
            "طائرة الكابوس", "طائرة النجوم", "طائرة الروك", 
"التنين الفريد", "الطائرة الحزامية", "مطار القاعدة السرية", 
"المطار السينمائي", "مطار الروك", "مطار المهرجان", "مطار الموديل"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedAirIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

        if choice == nil then return Air_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Stations_Menu() 
        end

        selectedAirIndex = choice
        local codes = air_mix_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Air_Selection_Loop()
    end

    Air_Selection_Loop()
end

-- ١. لیستی پاپۆڕ و لەنگەرەکان بە کوردی
local ship_island_list = {
    {1768641318, 1750294382, 1700753513, 1702130529, 842489714, 0}, -- پاپۆڕی جەژنی ئیستەر
    {1768641312, 1750294382, 1264545897, 1751607662, 116, 0},      -- پاپۆڕی سوارچاک
    {1768641310, 1750294382, 1784639593, 1851879521, 0, 0},        -- پاپۆڕی ژاپۆنی
    {1768641306, 1750294382, 1398763625, 14672, 0, 0},            -- پاپۆڕی گەشتیاری
    {1768641310, 1750294382, 1700753513, 1953528167, 0, 0},        -- پاپۆڕی میسری
    {1768641312, 1750294382, 1751085161, 1634495589, 115, 0},      -- پاپۆڕی یۆنانی
    {1768641322, 1632132974, 1919902322, 1935762783, 1601332596, 12855}, -- لەنگەری جەژنی ئیستەر
    {1768641316, 1632132974, 1919902322, 1768835935, 7628903, 0},      -- لەنگەری سوارچاک
    {1768641314, 1632132974, 1919902322, 1885432415, 28257, 0},        -- لەنگەری ژاپۆنی
    {1768641310, 1632132974, 1919902322, 961565535, 0, 0},             -- لەنگەری کەمەرەیی
    {1768641314, 1632132974, 1919902322, 2036819295, 29800, 0},        -- لەنگەری میسری
    {1768641322, 1632132974, 1919902322, 1919905375, 1197697380, 25711}  -- لەنگەری ڤایکینگ
}

local selectedShipIndex = 0

-- ٢. فەنکشنی پاپۆڕ و لەنگەر بە مێنۆی هەڵبژاردن
function Run_Ship_Island_Mixed()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local results = gg.getResults(1)
    
    if #results == 0 then 
        gg.setVisible(true)
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
        return Run_Stations_Menu() 
    end
    
    local cell3 = results[1].address + 12
    gg.addListItems({{address = cell3, flags = 4, value = 2, freeze = true}})
    
    local function Ship_Selection_Loop()
        local names = {
            "سفينة عيد الفصح", "سفينة الفارس", "السفينة اليابانية", "السفينة السياحية", 
"السفينة المصرية", "السفينة اليونانية", "مرسى عيد الفصح", "مرسى الفارس", 
"المرسى الياباني", "المرسى الحزامي", "المرسى المصري", "مرسى الفايكنج"

        }
        
        local displayNames = {}
        for i, name in ipairs(names) do
            displayNames[i] = (selectedShipIndex == i and "🔘 " or "⚪ ") .. name
        end
        table.insert(displayNames, "🔙 رجوع")

        gg.setVisible(false)
        local choice = gg.choice(displayNames, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

        if choice == nil then return Ship_Selection_Loop() end
        if choice == #displayNames then 
            gg.removeListItems(gg.getListItems())
            return Run_Stations_Menu() 
        end

        selectedShipIndex = choice
        local codes = ship_island_list[choice]
        
        gg.setValues({
            {address = cell3 + 4,  flags = 4, value = codes[1]},
            {address = cell3 + 8,  flags = 4, value = codes[2]},
            {address = cell3 + 12, flags = 4, value = codes[3]},
            {address = cell3 + 16, flags = 4, value = codes[4]},
            {address = cell3 + 20, flags = 4, value = codes[5]},
            {address = cell3 + 24, flags = 4, value = codes[6]}
        })

        gg.alert("​🙆🏻تم تبديل هدية 29 بنجاح، يجب أن تستلم الهدية خلال ثانيتين. افتح التصريح واستلم🙆🏻")
        gg.sleep(2500) 
        return Ship_Selection_Loop()
    end

    Ship_Selection_Loop()
end



--[[ 💎 SEROK ARAM LUXURY - STONE MINES 💎 ]]--

local isStoneSearched = false
local stoneResults = {}
local stoneConfig = {
    [1] = {name="⛏️ پاچ", hex={0x00326D04, 0, 0, 0, 0, 0}},
    [2] = {name="?? تەقینەوە", hex={0x00336D04, 0, 0, 0, 0, 0}},
    [3] = {name="🛢️ بەرمیل تەقینەوە", hex={0x00316D04, 0, 0, 0, 0, 0}}
}

-- ٢. فانکشنی سەرەکی مەنیو
function StoneMenu() 
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     ⛏️                    معول               ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🧨                 دینامیت              ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     💣               متفجرات                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄             رجــــــــــــوع                ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪               خـــــــــروج                ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return StoneMenu() end

    -- گەڕانەوە و پاککردنەوەی میمۆری
    if menu[4] then 
        isStoneSearched = false
        stoneResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("💐 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💐")
        if PdaistakanyYari then return PdaistakanyYari() end
        return 
    end

    if menu[5] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end
  
    -- پشکنینی هەڵبژاردن
    local anySelected = false
    for i=1, 3 do if menu[i] then anySelected = true break end end
    if not anySelected then return StoneMenu() end

    -- گەڕان تەنها بۆ یەکەم جار
    if not isStoneSearched then
        gg.clearResults()
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        
        local count = gg.getResultCount()
        if count == 0 then 
            isStoneSearched = false 
            gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ") 
            return StoneMenu()
        end
        stoneResults = gg.getResults(count)
        isStoneSearched = true
    end

    local input = gg.prompt({'أدخل الكمية المطلوبة:'}, {'0'}, {'number'})
    if not input then return StoneMenu() end

    local edit, freeze = {}, {}
    
    -- لۆژیکی ڕێگری لە تێکەڵبوونی کۆد
    local slotIdx = 1
    for i = 1, 3 do
        if menu[i] and stoneResults[slotIdx] then
            local v = stoneConfig[i]
            local r = stoneResults[slotIdx]
            
            table.insert(freeze, {address=r.address+12, value=2, flags=4, freeze=true})
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address=r.address+12+(j*4), value=h, flags=4}) 
            end
            table.insert(edit, {address=r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address=r.address+44, value=tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end
    
    if #edit > 0 then
        gg.setValues(edit) 
        gg.addListItems(freeze)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
        gg.setVisible(false)
        while not gg.isVisible() do
            gg.sleep(200) 
        end 
        return StoneMenu() 
    else
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return StoneMenu()
    end
end



 

local searchDone = false -- قوفڵکردن ی گەڕان بۆ ئەوەی دووبارە نەبێتەوە

function NaznawakanMenu()
    gg.setVisible(false)

    -- مەرج بۆ ئەوەی گەڕان تەنها یەکجار ئەنجام بدرێت
    if not searchDone then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        searchDone = true 
    end

    local r = gg.getResults(1)
    if #r == 0 then
        gg.alert(" ❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        searchDone = false -- ئەگەر نەیدۆزیەوە با بتوانێت دواتر گەڕان بکاتەوە
        return
    end

    -- فەنکشنی جێگیرکردنی نازناوەکان
    local function applyTitle(values)
        local t = {}
        for i, res in ipairs(r) do
            t[#t+1] = {address = res.address + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
            for j = 1, 6 do
                t[#t+1] = {address = res.address + 12 + (j * 4), flags = gg.TYPE_DWORD, value = values[j]}
            end
        end
        gg.setValues(t)
        gg.addListItems(t)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
    end

    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🦎  المستکشف الکرستالیە        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🦎     المستکشف الذهبيه        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🛥️     السفينه الكرستاليه           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🛥️         السفينه الذهبية          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ⚔️      السيوف  الأرجواني          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ⚔️           السيوف الذهبية        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🦇        الخفاش الأرجواني         ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🦇            الخفاش الذهبية        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄             رجــــــــــــوع                ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return end

    if menu[1] then applyTitle({1347962146, 1851871839, 926179179, 1634887519, 25710, 0}) end
    if menu[2] then applyTitle({1347962144, 1851871839, 926179179, 1935762015, 101, 0}) end
    if menu[3] then applyTitle({1347962146, 1851871839, 909401963, 1634887519, 25710, 0}) end
    if menu[4] then applyTitle({1347962144, 1851871839, 909401963, 1935762015, 101, 0}) end
    if menu[5] then applyTitle({1347962146, 1851871839, 959733611, 1634887519, 25710, 0}) end
    if menu[6] then applyTitle({1347962144, 1851871839, 959733611, 1935762015, 101, 0}) end
    if menu[7] then applyTitle({1347962146, 1851871839, 942956395, 1634887519, 25710, 0}) end
    if menu[8] then applyTitle({1347962144, 1851871839, 942956395, 1935762015, 101, 0}) end

    if menu[9] then 
        searchDone = false
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
        return PdaistakanyYari() 
    end

    -- بەشی وەستان (Sleep) تاوەکو مێنۆکە دەرنەچێت و دووبارە بێتەوە
    gg.setVisible(false)
    while true do
        if gg.isVisible() then
            gg.setVisible(false)
            return NaznawakanMenu()
        end
        gg.sleep(100)
    end
end


-- SLEMANI MENU - ARAM KURD TOWN (FULL V3)
gg.setVisible(false)

local targetAddress = nil
local pointerAddress = nil
local isReady = false
local currentMode = 0 -- 1: Timsal1, 2: Timsal2 (27), 3: Timsal3 (28)
local Slemani_SavedCopied = {}
local selectedIndex1, selectedIndex2, selectedIndex3 = 0, 0, 0

-- ١. لیستی تیمسالی ١
local LOCATIONS = {
{name = "معرض الحرف اليدوية 🎨", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350969, 829715041}},
{name = "سنترال بارك 🌳", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350961, 863269473}},
{name = "حفلة الشاطئ 🏖️", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881354545, 829715041}},
{name = "قلب إيطاليا 🇮🇹", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881354801, 829715041}},
{name = "موقع مخيم المريخ 🚀", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881354289, 829715041}},
{name = "صالة الديسكو 💃", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350968, 829715041}},
{name = "عالم البطريق 🐧", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350967, 846492257}},
{name = "مخيم الألعاب 🏕️", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350966, 846492257}},
{name = "المعرض الزراعي 🚜", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350965, 846492257}},
{name = "رحلة عشاق الطعام 🍕", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350964, 863269473}},
{name = "حديقة قوس قزح 🌈", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350963, 863269473}},
{name = "الحي الصيني 🏮", codes = {1735550285, 1698968165, 1634889571, 1852795252, 1881350962, 863269473}}
}
-- ٢. قائمة التماثيل ٢
local karim_PARTS = {
    {name = "ملكة جزيرة السلحفاة 🐢", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738994, 3372146}},
    {name = "حارس الشمال 🧊", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738995, 3241074}},
    {name = "أوديسة القراصنة 🏴‍☠️", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738996, 3241074}},
    {name = "❄️صخرة عملاق الثلج الكبيرة", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738997, 3241074}},
    {name = "👑 أسرار كليوباترا", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738998, 3241074}},
    {name = "منتزه الترفيه النباتي 🌿", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634738999, 3241074}},
    {name = "متحف مملكة بوسايدون 🔱", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634739000, 3241074}},
    {name = "مركز أبحاث الحالات النادرة 🪄", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1634739001, 3241074}}
}

-- ٣. لیستی تیمسالی ٣
local SMART_PARTS = {
{name = "القصر الذكي 🏰", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881354289, 829715041}},
{name = "منزل قرية الأيل الذهبي 🦌", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881354545, 829715041}},
{name = "نافورة اللوتس المتجمدة ❄️", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881354801, 829715041}},
{name = "مسرح باندورا القديم 🎭", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881355057, 829715041}},
{name = "البيت الزجاجي لمملكة آكل النحل 🐝", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881355313, 829715041}},
{name = "مؤسسة أبحاث الفضاء 🚀", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881355569, 829715041}},
{name = "مكتبة الشجرة 📚", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881355825, 829715041}},
{name = "قاعدة التخييم في الطبيعة 🏕️", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881356081, 829715041}},
{name = "المقهى الكوني ☕", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881356337, 829715041}},
{name = "الحديقة المائية لأرض القرود 🐒", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881356593, 829715041}},
{name = "الملاذ الجبلي 🏔️", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881354290, 829715041}},
{name = "حديقة الترفيه الفريدة 🎡", codes = {1701869637, 1769236836, 1698983535, 1634889571, 1852795252, 1881354546, 829715041}}
}
function Slemani_InitialSetup(mode)
    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
    gg.searchNumber("1599099688;1936682818;33;24", gg.TYPE_DWORD)
    gg.refineNumber("33", gg.TYPE_DWORD)
    local res1 = gg.getResults(1)
    if #res1 == 0 then gg.alert("🚫 دڵنیابەوە یاریەکەت بەسراوەتەوە بە جێم"); return false end
    
    for i = 0, 5 do
        local v = gg.getValues({{address = res1[1].address + (i * 4), flags = gg.TYPE_DWORD}})
        Slemani_SavedCopied[i+1] = v[1].value
    end

    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
    local res2 = gg.getResults(1)
    if #res2 == 0 then gg.alert("🚫 دڵنیابەوە یاریەکەت بەسراوەتەوە بە جێم"); return false end
    targetAddress = res2[1].address

    local middleCode = 33
    if mode == 2 then middleCode = 27 elseif mode == 3 then middleCode = 28 end

    gg.addListItems({{address = targetAddress + (3 * 4), flags = gg.TYPE_DWORD, value = 2, freeze = true}})
    gg.setValues({
        {address = targetAddress + (4 * 4), flags = gg.TYPE_DWORD, value = Slemani_SavedCopied[1]},
        {address = targetAddress + (5 * 4), flags = gg.TYPE_DWORD, value = Slemani_SavedCopied[2]},
        {address = targetAddress + (6 * 4), flags = gg.TYPE_DWORD, value = middleCode},
        {address = targetAddress + (7 * 4), flags = gg.TYPE_DWORD, value = Slemani_SavedCopied[4]},
        {address = targetAddress + (8 * 4), flags = gg.TYPE_DWORD, value = Slemani_SavedCopied[5]},
        {address = targetAddress + (9 * 4), flags = gg.TYPE_DWORD, value = Slemani_SavedCopied[6]}
    })

    gg.sleep(600)
    local pVal = gg.getValues({{address = targetAddress + (8 * 4), flags = gg.TYPE_QWORD}})
    pointerAddress = pVal[1].value
    if pointerAddress == 0 or pointerAddress == nil then return false end

    isReady = true
    currentMode = mode
    gg.toast("✅ جاهز لتمثال " .. mode)
    return true
end

function ApplyLocation(index, listType)
    local list = LOCATIONS
    if listType == 2 then list = karim_PARTS elseif listType == 3 then list = SMART_PARTS end
    local loc = list[index]
    local editList = {}
    for j = 1, #loc.codes do
        editList[j] = {address = pointerAddress + ((j - 1) * 4), flags = gg.TYPE_DWORD, value = loc.codes[j]}
    end
    gg.setValues(editList)
    
    -- ئەم دێڕە لێرەدا زیاد کرا بۆ ئەوەی دیارییەکە فریز بکات و بەتاڵ نەبێت
    gg.addListItems(editList)
    
    -- پەنجەرە گەورەکەت لێرەدا جێگیر کرا
    gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
end
-- ================= مێنۆ لاوەکییەکان =================

function Slemani_Sub1()
    gg.setVisible(false)
    if not isReady or currentMode ~= 1 then if not Slemani_InitialSetup(1) then return end end
    local names = {}
    for i, v in ipairs(LOCATIONS) do names[i] = (selectedIndex1 == i and "🔘 " or "⚪ ") .. v.name end
    table.insert(names, "🔙 رجوع")
    
    local choice = gg.choice(names, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    if choice == nil then return end
    
    if choice == #names then 
        gg.clearResults() 
        gg.clearList()
        return Slemani_Main() 
    end
    
    selectedIndex1 = choice
    ApplyLocation(choice, 1)

    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
    return Slemani_Sub1()
end

function Slemani_Sub2()
    gg.setVisible(false)
    if not isReady or currentMode ~= 2 then if not Slemani_InitialSetup(2) then return end end
    local names = {}
    for i, v in ipairs(karim_PARTS) do names[i] = (selectedIndex2 == i and "🔘 " or "⚪ ") .. v.name end 
    table.insert(names, "🔙 رجوع")
    
    local choice = gg.choice(names, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    if choice == nil then return end
    
    if choice == #names then 
        gg.clearResults() 
        gg.clearList()
        return Slemani_Main() 
    end
    
    selectedIndex2 = choice
    ApplyLocation(choice, 2)
    
    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
    return Slemani_Sub2()
end

function Slemani_Sub3()
    gg.setVisible(false)
    if not isReady or currentMode ~= 3 then if not Slemani_InitialSetup(3) then return end end
    local names = {}
    for i, v in ipairs(SMART_PARTS) do names[i] = (selectedIndex3 == i and "🔘 " or "⚪ ") .. v.name end
    table.insert(names, "🔙 رجوع")
    
    local choice = gg.choice(names, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    if choice == nil then return end
    
    if choice == #names then 
        gg.clearResults() 
        gg.clearList()
        return Slemani_Main() 
    end
    
    selectedIndex3 = choice
    ApplyLocation(choice, 3)
    
    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
    return Slemani_Sub3()
end
-- ================= مێنۆی سەرەکی =================

function Slemani_Main()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🗿           التمثال الأول             ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🗿           التمثال الثاني             ꕤ\n╚══════════════════════╝",
        "╔══════════ ??══════════╗\nꕤ     🗿           التمثال الثالث             ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     ↩️             رجـــــــــــوع                 ꕤ\n╚══════════════════════╝",
        
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

    if menu == nil then return end

    if menu[1] then Slemani_Sub1() end
    if menu[2] then Slemani_Sub2() end
    if menu[3] then Slemani_Sub3() end
    
    if menu[4] then 
        gg.clearResults() 
        gg.clearList()
        return PdaistakanyYari() 
    end

    gg.setVisible(false)
    while not gg.isVisible() do gg.sleep(200) end
    return Slemani_Main()
end

        
-- لێرەوە دەست پێ دەکات

function applyBadge(values, results)
    local t = {}
    for i, res in ipairs(results) do
        t[#t+1] = {address = res.address + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
        for j = 1, 6 do
            t[#t+1] = {address = res.address + 12 + (j * 4), flags = gg.TYPE_DWORD, value = values[j]}
        end
    end
    gg.setValues(t)
    gg.addListItems(t)
    gg.toast("✅ تم بنجاح")
end

function Aram_Logokan()
    -- ١. پاککردنەوەی میمۆری لە کاتی چوونە ناو ئەم بەشە
    gg.clearResults()
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)

    local r = gg.getResults(100)
    if #r == 0 then
        gg.alert("❌ لم يتم العثور على أي نتائج!")
        return 
    end

    local firstRun = true

    while true do
        if firstRun or gg.isVisible(true) then
            firstRun = false
            gg.setVisible(false)
            
            local menu = gg.multiChoice({
          "١. علامة الرحلة",
"٢. علامة الرحلة الأسطورية",
"٣. علامة البلدية الأسطورية",
"٤. علامة المدينة",
"٥. علامة منزل العمدة (أصفر)",
"٦. علامة الشتاء الأسطورية",
"٧. علامة الشتاء",
"٨. علامة منزل العمدة (أرجواني)",
"٩. علامة الطبخ",
"١٠. علامة الطبخ الأسطورية",
"🔙 الرجوع ومسح الذاكرة" 
}, nil, "🛠 شعارات الاسم")


            if menu == nil then return end

            if menu[1] then applyBadge({1684103708, 811558247, 1919377203, 6581857, 0, 0}, r) end
            if menu[2] then applyBadge({1684103706, 811558247, 1633836851, 25971, 0, 0}, r) end
            if menu[3] then applyBadge({1684103708, 811558247, 1919377201, 6581857, 0, 0}, r) end
            if menu[4] then applyBadge({1684103706, 811558247, 1633836849, 25971, 0, 0}, r) end
            if menu[5] then applyBadge({1684103712, 811558247, 846618417, 1935762015, 101, 0}, r) end
            if menu[6] then applyBadge({1684103708, 811558247, 1919377202, 6581857, 0, 0}, r) end
            if menu[7] then applyBadge({1684103706, 811558247, 1633836850, 25971, 0, 0}, r) end
            if menu[8] then applyBadge({1684103714, 811558247, 846618417, 1634887519, 25710, 0}, r) end
            if menu[9] then applyBadge({1684103706, 811558247, 1633836853, 25971, 0, 0}, r) end
            if menu[10] then applyBadge({1684103708, 811558247, 1919377205, 6581857, 0, 0}, r) end
            
            if menu[11] then 
                gg.clearResults() 
                gg.clearList()
                gg.toast("🧹 تم تنظيف الذاكرة")
                return 
            end
        end
        gg.sleep(200) -- 🛡️ دژە کڕاش
    end
end



-- ARAM KURD TOWN - POINTER SYNC (CELL 3 FROZEN)






    function MainMenu()
            
            local menu = gg.multiChoice({
            	"╔══════════ 🦋══════════╗\nꕤ     🎫     فتح التذكره الذهبيه         ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ  رفع المستوى مع فتح الأراضي   ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🌾  زياده المستوي من الزراعة  ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🚁 زياده المستوي من الطائرة  ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🕣   ارسل الكروت بدون وقت     ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     📚          زياده الكروت                ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🧰     اكواد الأكياس للكروت      ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ🚉      طلب قمح من التعاون          ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👷      فتح المباني المجتمعه   ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ   🚂   طلب مساعده في القطار     ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ🚉 طلب رفع المستوي في القطار ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🏜️          توسيع الاراضي            ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🏡            توسيع الشونه ثابت   ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🏜️          توسيع الشونە مؤقت  ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🕰️       اكواد تصفير الوقت         ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🕹️      الكاش☜الفلوس☜إلخ     ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👷        ضعف النقاط  هدية       ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👑       زيادة نقاط السباق          ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👑       زيادة عدد الإعجابات       ꕤ\n╚══════════════════════╝",        
                "╔══════════ 🦋══════════╗\nꕤ     👷    إرسال الهيلو بدون طلب    ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👷   زیادة عدد صناديق السوق  ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     👷زیادة عدد صناديق المعمل  ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🛠️      مستلزمات داخل اللعبة   ꕤ\n╚══════════════════════╝",
                "╔══════════ 🦋══════════╗\nꕤ     🚪             خــــــــــروج                 ꕤ\n╚══════════════════════╝",

            }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

            if menu == nil then       
                gg.setVisible(false) 
            else
                if menu[1] == true then HackGoldPass() end
                if menu[2] then jalalhh() end
                if menu[3] == true then WheatLevelXP() end
                if menu[4] == true then HackLogic() end
                if menu[5] == true then Nardni_Kart() end
                if menu[6] == true then CardHack() end
                if menu[7] == true then CardsSystemAram() end
                if menu[8] then talbganm() end
                if menu[9] == true then OpenYellowHats() end
                if menu[10] == true then HackTrain() end
                if menu[11] == true then gg.setVisible(true) Hacklivl() end
                if menu[12] == true then OpenAllLands() end
                if menu[13] == true then Koga() end
                if menu[14] == true then shuunaa() end
                if menu[15] then SubMenu12() end
                if menu[16] then MenuZyadkrdn() end
                if menu[17] then X2() end
                if menu[18] then kurd() end
                if menu[19] then likat() end
                if menu[20] then tayarrrrr() end
                if menu[21] then snduqsuq() end
                if menu[22] then snduqmasna3() end
                if menu[23] then PdaistakanyYari() end
                if menu[24] == true then 
              gg.clearList()   
       gg.clearResults() 
      gg.toast("👋 في أمان الله، لا تنسانا من صالح دعائك")
  os.exit() 
end
        end
        gg.sleep(100)    
    end



function HackLogic()

    -- لافیتەی ئاگادارکردنەوە
    gg.alert("🚁 أهلاً بك\n\n⚠️ تأكد من فتح خانة الطلب (٢) قبل الاستمرار.")

    local input = gg.prompt({
        "💰 كمية الذهب (900000):",
        "💵 كمية الكاش (850000):",
        "⭐ كمية المستوى (30000000):"
    }, {
        900000,
        850000,
        30000000
    }, {
        "number",
        "number",
        "number"
    })

    if input == nil then
        return
    end

    gg.clearResults()

    -- هەمان Memory Region ـەی وێنەکەت: Ca + O
    gg.setRanges(
        gg.REGION_C_ALLOC | gg.REGION_OTHER
    )

    -- گەڕان بۆ تەڵەبەکە
    gg.searchNumber(
        "1703939;0;0;0;2;0::45",
        gg.TYPE_DWORD
    )

    local n = gg.getResultCount()

    if n == 0 then

        gg.alert(
            "❌ لم يتم العثور عليه!\n\n" ..
            "تأكد من أن خانة الطلب (٢) مفتوحة."
        )

        gg.clearResults()
        MainMenu()
        return
    end

    local results = gg.getResults(1)

    if results == nil or #results == 0 then
        gg.alert("❌ تعذر الحصول على النتيجة.")
        gg.clearResults()
        MainMenu()
        return
    end

    local base = results[1].address

    local modifications = {

        -- گۆڕینی نرخەکان
        {address = base + 0x30, value = 0,          flags = gg.TYPE_DWORD},
        {address = base + 0x34, value = input[1],   flags = gg.TYPE_DWORD},

        {address = base + 0x38, value = 0,          flags = gg.TYPE_DWORD},
        {address = base + 0x3C, value = input[2],   flags = gg.TYPE_DWORD},

        {address = base + 0x50, value = 0,          flags = gg.TYPE_DWORD},
        {address = base + 0x54, value = input[3],   flags = gg.TYPE_DWORD}
    }

    gg.setValues(modifications)

    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 💮")

    gg.clearResults()
    MainMenu()
end
-- [[ 🚂 بەشی قیتار لێرە دەستپێدەکات ]]
function HackTrain()

gg.setVisible(false)
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.clearResults()
    gg.searchNumber("50;1801519104;51;52:65", gg.TYPE_DWORD)
    gg.refineNumber("51", gg.TYPE_DWORD)

    local results = gg.getResults(3)

    if #results == 0 then
        gg.toast("❌ لم يتم العثور على المؤش")
        return
    end

    local freezeList = {}

    for i, v in ipairs(results) do

    local modifications = {
    {address = v.address + 52, flags = gg.TYPE_FLOAT, value = 1, freeze = true},

    
    {address = v.address - 388, flags = gg.TYPE_QWORD, value = 1, freeze = true},
    {address = v.address - 340, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    {address = v.address - 408, flags = gg.TYPE_DWORD, value = 1677751393, freeze = true},
    {address = v.address - 412, flags = gg.TYPE_DWORD, value = 1701345034, freeze = true},

    {address = v.address - 644, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 692, flags = gg.TYPE_QWORD, value = 1, freeze = true},
    {address = v.address - 712, flags = gg.TYPE_DWORD, value = 1677751393, freeze = true},
    {address = v.address - 716, flags = gg.TYPE_DWORD, value = 1701345034, freeze = true},

    {address = v.address - 948, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 996, flags = gg.TYPE_QWORD, value = 1, freeze = true},
    {address = v.address - 1016, flags = gg.TYPE_DWORD, value = 1677751393, freeze = true},
    {address = v.address - 1020, flags = gg.TYPE_DWORD, value = 1701345034, freeze = true},

    {address = v.address - 1252, flags = gg.TYPE_DWORD, value = 1, freeze = true},


    {address = v.address - 1300, flags = gg.TYPE_QWORD, value = 1, freeze = true},
    {address = v.address - 1320, flags = gg.TYPE_DWORD, value = 1677751393, freeze = true},
    {address = v.address - 1324, flags = gg.TYPE_DWORD, value = 1701345034, freeze = true},

    {address = v.address - 1556, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 1604, flags = gg.TYPE_QWORD, value = 1, freeze = true},
    {address = v.address - 1624, flags = gg.TYPE_DWORD, value = 1677751393, freeze = true},
    {address = v.address - 1628, flags = gg.TYPE_DWORD, value = 1701345034, freeze = true},
}

        gg.setValues(modifications)

        for _, mod in ipairs(modifications) do
            if mod.freeze then
                table.insert(freezeList, {
                    address = mod.address,
                    flags = mod.flags,
                    value = mod.value,
                    freeze = true
                })
            end
        end
    end

    if #freezeList > 0 then
        gg.addListItems(freezeList)
        gg.alert("👸 مبروك طلب القيتار تم بنجاح 👸")
    else
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    end
end



 -- ==========================================
-- قیتاری زیادکردنی مستوا لێرەوە دەست پێ دەکات
-- ==========================================
function Hacklivl()


gg.setVisible(false)
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.clearResults()
    gg.searchNumber("50;1801519104;51;52:65", gg.TYPE_DWORD)
    gg.refineNumber("51", gg.TYPE_DWORD)

    local results = gg.getResults(3)

    if #results == 0 then
        gg.toast("❌ لم يتم العثور على المؤش")
        return
    end

    local freezeList = {}

    for i, v in ipairs(results) do

    local modifications = {
    {address = v.address + 52, flags = gg.TYPE_FLOAT, value = 1, freeze = true},

    
    {address = v.address - 388, flags = gg.TYPE_QWORD, value = 500, freeze = true},
    {address = v.address - 340, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    {address = v.address - 408, flags = gg.TYPE_DWORD, value = 103, freeze = true},
    {address = v.address - 412, flags = gg.TYPE_DWORD, value = 1852404232, freeze = true},

    {address = v.address - 644, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 692, flags = gg.TYPE_QWORD, value = 500, freeze = true},
    {address = v.address - 712, flags = gg.TYPE_DWORD, value = 103, freeze = true},
    {address = v.address - 716, flags = gg.TYPE_DWORD, value = 1852404232, freeze = true},

    {address = v.address - 948, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 996, flags = gg.TYPE_QWORD, value = 500, freeze = true},
    {address = v.address - 1016, flags = gg.TYPE_DWORD, value = 103, freeze = true},
    {address = v.address - 1020, flags = gg.TYPE_DWORD, value = 1852404232, freeze = true},

    {address = v.address - 1252, flags = gg.TYPE_DWORD, value = 1, freeze = true},


    {address = v.address - 1300, flags = gg.TYPE_QWORD, value = 500, freeze = true},
    {address = v.address - 1320, flags = gg.TYPE_DWORD, value = 103, freeze = true},
    {address = v.address - 1324, flags = gg.TYPE_DWORD, value = 1852404232, freeze = true},

    {address = v.address - 1556, flags = gg.TYPE_DWORD, value = 1, freeze = true},

    
    {address = v.address - 1604, flags = gg.TYPE_QWORD, value = 500, freeze = true},
    {address = v.address - 1624, flags = gg.TYPE_DWORD, value = 103, freeze = true},
    {address = v.address - 1628, flags = gg.TYPE_DWORD, value = 1852404232, freeze = true},
}

        gg.setValues(modifications)

        for _, mod in ipairs(modifications) do
            if mod.freeze then
                table.insert(freezeList, {
                    address = mod.address,
                    flags = mod.flags,
                    value = mod.value,
                    freeze = true
                })
            end
        end
    end

    if #freezeList > 0 then
        gg.addListItems(freezeList)
        gg.alert("👸 مبروك طلب القيتار تم بنجاح 👸")
    else
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    end
end

-- ==========================================
function HackGoldPass()

    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.clearResults()
gg.setVisible(false)
gg.searchNumber("1937011470;1701998435", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("1937011470", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
local results = gg.getResults(gg.getResultCount())
if #results == 0 then
gg.alert("❌ لم يتم العثور على المؤش")
return
end
local success = false
for i, v in ipairs(results) do
local offset232 = gg.getValues({{address = v.address + 232, flags = gg.TYPE_DWORD}})[1]
local offset236 = gg.getValues({{address = v.address + 236, flags = gg.TYPE_DWORD}})[1]
local offset240 = gg.getValues({{address = v.address + 240, flags = gg.TYPE_DWORD}})[1]
local offset244 = gg.getValues({{address = v.address + 244, flags = gg.TYPE_DWORD}})[1]

if offset232.value and offset236.value and offset240.value and offset244.value then
local str232 = tostring(math.abs(offset232.value))
local str236 = tostring(math.abs(offset236.value))
local str240 = tostring(math.abs(offset240.value))
local str244 = tostring(math.abs(offset244.value))

local length232 = #str232
local length236 = #str236
local length240 = #str240
local length244 = #str244

local validLength232 = (length232 == 8 or length232 == 9 or length232 == 10)
local validLength236 = (length236 == 8 or length236 == 9 or length236 == 10)
local validLength240 = (length240 == 8 or length240 == 9 or length240 == 10)
local validLength244 = (length244 == 8 or length244 == 9 or length244 == 10)

local isMatchFirstPair = str232:sub(1, 4) == str236:sub(1, 4)
local isMatchSecondPair = str240:sub(1, 4) == str244:sub(1, 4)
if validLength232 and validLength236 and validLength240 and validLength244 and isMatchFirstPair and isMatchSecondPair then  
          
gg.setValues({{address = v.address + 232, flags = gg.TYPE_QWORD, value = 1000},
{address = v.address + 248, flags = gg.TYPE_DWORD, value = 1}})
success = true
end
end
end
if success then
gg.alert("💮 🏆💛مبروك تم فتح التذكرة الذهبية 💛🏆💮")
gg.toast("💮 🏆💛مبروك تم فتح التذكرة الذهبية 💛🏆💮")
else
gg.alert("❌ لم يتم العثور على المؤشم")
end
gg.clearList()
 gg.clearResults()
 end

---------------------------------------------------------
-- 🌾 هاکی گەنم و مستوا لێرەوە دەست پێ دەکات 🌾 --
---------------------------------------------------------

function WheatLevelXP()
   
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.clearResults()
gg.setVisible(false)

gg.searchNumber('1701147414;2002744164;1123024896', gg.TYPE_DWORD) 
gg.refineNumber('1123024896', gg.TYPE_DWORD)
n = gg.getResultCount()
if n == 0 then
gg.alert("❌ لم يتم العثور على المؤشم")
gg.clearResults()
return
end
gg.toast(n)
jz = gg.getResults(n)
local messageShown = false 
local toastShown = false 
local M12 = gg.prompt({"💮 🄳🄸🄳??🅁🅆🄰🄷🄰🄱💮"},{[1]="\n  0 \n"},nil,{'number'})
if M12 == nil then
else
end
if M12[1] ==nil then
else
end
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address + 0,flags = gg.TYPE_DWORD,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 16,flags = gg.TYPE_QWORD,freeze = true,value = M12[1],gg.TYPE_QWORD}})
if not messageShown then
if not toastShown then

gg.alert(" 🌾 ازراع قمحا واحصده الزيادة مستوا مدينتك 🌾")
toastShown = true
messageShown = true 
end 
end
end
gg.clearList()
gg.clearResults()
end 

---------------------------------------------------------
-- 🔚 کۆتایی بەشی هاکی گەنم ?? --
---------------------------------------------------------
-- لێرەوە اسکریپ ناردنی کارت بێ کات دەست پێ دەکات
function Nardni_Kart()
   
    
    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.clearResults()
    gg.setVisible(false)

    -- گەڕانی نوێ (بەکارهێنانی شیوازی تخصیص بۆ هێکسا/گشتی)
    gg.searchNumber("168429571X20h", gg.TYPE_DWORD)
    gg.refineNumber("1701274988", gg.TYPE_DWORD)

    local n_new = gg.getResultCount()
    
    if n_new == 0 then
        gg.toast("❌ لم يتم العثور على نتائج للبحث❌")
        gg.clearResults()
    else
        local r_new = gg.getResults(n_new)
        for i = 1, n_new do
            r_new[i].value = 0
            r_new[i].freeze = true
        end
        gg.setValues(r_new)
        gg.addListItems(r_new)
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
        gg.clearResults()
    end

    -- تغير الكارت الذهبي 
    --الكود الاول 
    gg.searchNumber("1684827975;1701667150;1684828007:73", gg.TYPE_DWORD)
    gg.refineNumber("1684828007", gg.TYPE_DWORD)

    local n1 = gg.getResultCount()

    
    if n1 == 0 then
        gg.clearResults()
        --الكود الثاني 
        gg.searchNumber("1684828007;0;0:9", gg.TYPE_DWORD)
        gg.refineNumber("1684828007", gg.TYPE_DWORD)
        n1 = gg.getResultCount()
    end

    
    if n1 == 0 then
        gg.alert("🤦‍♂️🤦‍♂️🤦‍♂️🤦‍♂️🤦‍♂️")
        gg.clearResults()
    else
        local r1 = gg.getResults(n1)
        for i = 1, n1 do
            r1[i].value = 2003790951
        end
        gg.setValues(r1)
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
        gg.clearResults()
    end

    -- ارسال الكروت 
    gg.toast("💮 ??🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.searchNumber("86400;50;1;1;1::17", gg.TYPE_DWORD)
    gg.refineNumber("86400", gg.TYPE_DWORD)

    local n2 = gg.getResultCount()
    if n2 == 0 then
        gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
        gg.clearResults()
        return
    end

    local r2 = gg.getResults(n2)
    local offsets = {32, 36, 40, 44, 48, 52}
    local edits = {}

    for i = 1, n2 do
        local base = r2[i].address
        for _, off in ipairs(offsets) do
            table.insert(edits, {
                address = base + off,
                flags = gg.TYPE_DWORD,
                value = 0,
                freeze = true
            })
        end
    end

    gg.setValues(edits)
    gg.addListItems(edits)

    gg.alert("🔥 الان يمكنك ارسال الكروت 🔥")
    gg.clearResults()
end
---------------------------------------------------------
-- 🛡️ لێرەوە کردنەوەی زەوی دەست پێ دەکات 🛡️ --
---------------------------------------------------------

function OpenAllLands()

    gg.clearResults()
    gg.toast("لا تنسانا من صالح دعائك 🤲")
    gg.searchNumber("1886938387x368", gg.TYPE_DWORD)
    
    local count = gg.getResultCount()
    
    -- پشکنینی ئەوەی ئایا ئەنجام دۆزراوەتەوە یان نا
    if count == 0 then
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return
    end

    -- سقلکردنی ئەنجامەکان بۆ ژمارە 1
    gg.refineNumber("1", gg.TYPE_DWORD)
    count = gg.getResultCount()
    
    if count == 0 then
        gg.alert("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    else
        -- گۆڕینی هەموو ئەو ئەنجامانەی کە ماونەتەوە بۆ 6
        local results = gg.getResults(count)
        local editList = {}
        
        for i, v in ipairs(results) do
            table.insert(editList, {
                address = v.address, 
                flags = v.flags, 
                value = 6
            })
        end
        
        gg.setValues(editList)
        gg.toast("✅ تم فتح جميع الأراضي بنجاح")
        gg.clearResults()
    end
end

---------------------------------------------------------
-- 🏁 کۆتایی بەشی کردنەوەی زەوی 🏁 --
---------------------------------------------------------
-- فەنکشنی تایبەت بە زیادکردنی کارت (Aram & Mahmoud)
function CardHack()
    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.setVisible(false)
gg.clearResults()

    pcall(function()
    gg.searchNumber("1918984974~1918984976", gg.TYPE_DWORD)
    end)

    local total = gg.getResultsCount()
    if total == 0 then
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return
    end

    local batchSize = 200
    local valid = {}


    for i = 1, total, batchSize do
        local size = math.min(batchSize, total - i + 1)

        local part = {}
        pcall(function()
            part = gg.getResults(size, i - 1)
        end)

        if part and #part > 0 then
            local readList = {}

            for _, v in ipairs(part) do
                readList[#readList+1] = {address = v.address + 24, flags = gg.TYPE_DWORD}
                readList[#readList+1] = {address = v.address + 32, flags = gg.TYPE_DWORD}
            end

            local values = {}
            pcall(function()
                values = gg.getValues(readList)
            end)

            if values and #values > 0 then
                local index = 1

                for j = 1, #values, 2 do
                    local val24 = tonumber(values[j].value) or -1
                    local val32 = tonumber(values[j+1].value) or 0

                    if val24 >= 0 and val24 <= 10 and val32 > 0 then
                        valid[#valid+1] = part[index]
                    end

                    index = index + 1
                end
            end
        end
    end

    if #valid == 0 then
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return
    end

      
 
   local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
   
    if not input or not input[1] then
        gg.clearResults()
        return
    end

    local newVal = tonumber(input[1])
    if not newVal then
        gg.toast("🤦‍♂️🤦‍♂️🤦‍♂️🤦‍♂️")
        return
    end

    
    if newVal > 999999 then newVal = 999999 end
    if newVal < 0 then newVal = 0 end

    
    local edits = {}
    for _, item in ipairs(valid) do
        edits[#edits+1] = {
            address = item.address + 28,
            flags = gg.TYPE_DWORD,
            value = newVal
        }
    end


    pcall(function()
        gg.setValues(edits)
    end)
    gg.alert("🙋‍♂️تم زيادة الكروت بنجاح 🙋‍♂️")
    gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
    gg.clearResults()
end


-- گۆڕینی ناوەکان بۆ ئەوەی تێکەڵ نەبن
local isSearchedCards = false
local cardsResults = {}
local configCards = {
    [1] = {name="الكيس البرونزيز", hex={1918976790, 1348420452, 829121377, 0, 0, 0}},
    [2] = {name="الكيس الأخضر", hex={1918976790, 1348420452, 845898593, 0, 0, 0}},
    [3] = {name="الكيس الأزرق ", hex={1918976790, 1348420452, 862675809, 0, 0, 0}},
    [4] = {name="الكيس البنفسجي", hex={1918976790, 1348420452, 879453025, 0, 0, 0}},
    [5] = {name="الكيس الذهبي", hex={1918976790, 1348420452, 896230241, 0, 0, 0}}
}

-- ناوی فەنکشنەکە CardsSystemAram
function CardsSystemAram()
    gg.setVisible(false)
    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🟤          الكيس البرونزي           ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🟢           الكيس الأخضر            ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔵             الكيس الأزرق            ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🟣        الكيس البنفسجي          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🟡            الكيس الذهبي          ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄             رجــــــــــوع                 ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🚪             خــــــــــروج                 ꕤ\n╚══════════════════════╝",
       
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")
    
    if menu == nil then return CardsSystemAram() end

    -- گەڕانەوە و پاککردنەوەی میمۆری
    if menu[6] then 
        isSearchedCards = false
        cardsResults = {}
        gg.clearResults()
        gg.clearList()
        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
        if MainMenu then return MainMenu() end 
        return 
    end

    if menu[7] then 
        gg.clearList() 
        gg.clearResults() 
        os.exit() 
    end
    
    local anySelected = false
    for i=1, 5 do if menu[i] then anySelected = true break end end
    if not anySelected then return CardsSystemAram() end

    -- گەڕان تەنها بۆ یەکەم جار
   if not isSearchedCards then

    gg.clearResults()

    -- هەمان Memory Region ـی Ca,O
    gg.setRanges(
        gg.REGION_C_ALLOC | gg.REGION_OTHER
    )

    gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)

    gg.refineNumber(
        "29",
        gg.TYPE_DWORD
    )

    local count = gg.getResultCount()

    if count == 0 then
        isSearchedCards = false
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن")
        return CardsSystemAram()
    end

    cardsResults = gg.getResults(count)
    isSearchedCards = true
end

    local input = gg.prompt({'اكتب الكمية المطلوبة:'}, {'0'}, {'number'})
    if input == nil then return CardsSystemAram() end

    local edit = {}
    local freeze = {}

    -- لۆژیکی ڕێگری لە تێکەڵبوونی کۆد
    local slotIdx = 1
    for i = 1, 5 do
        if menu[i] and cardsResults[slotIdx] then
            local v = configCards[i]
            local r = cardsResults[slotIdx]
            
            table.insert(freeze, {address = r.address + 12, value = 2, flags = 4, freeze = true})
            for j, h in ipairs(v.hex) do 
                table.insert(edit, {address = r.address + 12 + (j * 4), value = h, flags = 4}) 
            end
            table.insert(edit, {address = r.address + 40, value = 0, flags = 4})
            table.insert(edit, {address = r.address + 44, value = tonumber(input[1]), flags = 4})
            
            slotIdx = slotIdx + 1
        end
    end
    
    if #edit > 0 then
    gg.setValues(edit)
    gg.addListItems(freeze)
    
    -- پەنجەرە گەورەکە لێرەدا جێگیر کرا
    gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
    
    gg.setVisible(false)
    while not gg.isVisible() do
        gg.sleep(200)
    end
    return CardsSystemAram()
    else
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        return CardsSystemAram() 
    end
end


--------------------------------------------------
-- 👷 کڵاوە زەردەکان لێرەوە دەست پێ دەکات 👷 --
--------------------------------------------------

function OpenYellowHats()
    gg.alert("الرجاء التأكد من فتح نافذة القبعات الصفراء")
    
gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎️")
gg.clearResults()
gg.setVisible(false)
gg.searchNumber('256;1836016402::81', gg.TYPE_DWORD)
gg.refineNumber("256", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
n = gg.getResultCount()
if n == 0 then
gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
gg.clearResults()
return
end
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address + 24, flags = gg.TYPE_DWORD, freeze = true, value = 4}})
gg.addListItems({[1] = {address = jz[i].address + 32, flags = gg.TYPE_QWORD, freeze = true, value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 40, flags = gg.TYPE_QWORD, freeze = true, value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 48, flags = gg.TYPE_QWORD, freeze = true, value = 0}})
end
gg.alert("🏠 اذهب الآن إلى جميع المباني المجتمعية وقم بفتحها.")
gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎")
gg.clearResults()
end
--------------------------------------------------
-- 👷 کۆتایی کۆدی کڵاوە زەردەکان 👷 --
--------------------------------------------------

function Koga()
gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎️")
    gg.clearResults()
    gg.setVisible(false)
    
    gg.searchNumber("50;1;70;2;90;3;110;4::113", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber("50", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)

    local n = gg.getResultCount()

    
    if n == 0 then
        gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
        gg.clearResults()
        return
    end

    local startOffset = gg.getResults(1)[1].address
    local endOffset = startOffset + 0xC60
    
    
    local modifications = {}
    for offset = 0, 0xC60, 4 do
        table.insert(modifications, {
            address = startOffset + offset,
            flags = gg.TYPE_DWORD,
            value = 0
        })
    end

    gg.setValues(modifications)

    gg.alert("🌾✨ الآن يمكنك توسيع الشونة حسب حاجتك لتجنّب الحظر! 🚜📦🔄 تظهر التغييرات بعد إغلاق المدينة وفتحها من جديد. 🔓🏡")
    
    gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ ")

    gg.clearResults()
    gg.clearList()
end
-- Township Universal Time Reset
-- Created for: Aram


local saved_base2 = nil
local saved_copied = nil

function Binakan()

    if saved_copied == nil or saved_base2 == nil then
        gg.clearResults()
        


        gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ ")
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber("1599099692;1936682818;1701860212;1884644453;33;24", gg.TYPE_DWORD)
        gg.refineNumber("24", gg.TYPE_DWORD)

        local r1 = gg.getResults(1)
        if #r1 == 0 then
            gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن ")
            return
        end

        local addr1 = r1[1].address
        saved_copied = gg.getValues({
            {address = addr1 - 8, flags = gg.TYPE_DWORD},
            {address = addr1 - 4, flags = gg.TYPE_DWORD},
            {address = addr1,     flags = gg.TYPE_DWORD},
            {address = addr1 + 4, flags = gg.TYPE_DWORD},
            {address = addr1 + 8, flags = gg.TYPE_DWORD},
            {address = addr1 + 12, flags = gg.TYPE_DWORD}
        })

        -- گەڕان بۆ بەهای ئامانج (29)
        gg.clearResults()
        gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ ")
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)

        local r2 = gg.getResults(1)
        if #r2 == 0 then
            gg.alert("لم يتم العثور على القيمة المستهدفة (29)!")
            saved_copied = nil 
            return
        end
        saved_base2 = r2[1].address
    end


    local input = gg.prompt({"حدد القيمة "}, {0}, {"number"})
    
    if input then

        gg.clearList()
        
        local p = {}
        local b = saved_base2
        

        p[1] = {address = b + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
        p[2] = {address = b + 16, flags = gg.TYPE_DWORD, value = saved_copied[1].value, freeze = true}
        p[3] = {address = b + 20, flags = gg.TYPE_DWORD, value = saved_copied[2].value, freeze = true}
        p[4] = {address = b + 24, flags = gg.TYPE_DWORD, value = saved_copied[3].value, freeze = true}
        p[5] = {address = b + 28, flags = gg.TYPE_DWORD, value = saved_copied[4].value, freeze = true}
        p[6] = {address = b + 32, flags = gg.TYPE_DWORD, value = saved_copied[5].value, freeze = true}
        p[7] = {address = b + 36, flags = gg.TYPE_DWORD, value = saved_copied[6].value, freeze = true}
        p[8] = {address = b + 40, flags = gg.TYPE_DWORD, value = 0, freeze = true}
        p[9] = {address = b + 44, flags = gg.TYPE_DWORD, value = input[1], freeze = true}

        gg.addListItems(p)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        gg.clearResults()
    end
end


function Agriculture()
    if saved_base2 == nil then
        gg.clearResults()
      
        gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ ")
        
  gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)

        local results = gg.getResults(1)
        if #results == 0 then
            gg.alert("لم يتم العثور على الكود المطلوب! ❌")
            return
        end
        saved_base2 = results[1].address
    end

    local input = gg.prompt({"🕐 أدخل مقدار الوقت"}, {0}, {"number"})
    
    if input then
        gg.clearList() 
        local p = {}
        local b = saved_base2
        

        p[1] = {address = b + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
        

        p[2] = {address = b + 16, flags = gg.TYPE_DWORD, value = 0x5F50532C} -- خانەی ٤
        p[3] = {address = b + 20, flags = gg.TYPE_DWORD, value = 0x736F6F42} -- خانەی ٥
        p[4] = {address = b + 24, flags = gg.TYPE_DWORD, value = 0x65705374} -- خانەی ٦
        p[5] = {address = b + 28, flags = gg.TYPE_DWORD, value = 0x70556465} -- خانەی ٧
        p[6] = {address = b + 32, flags = gg.TYPE_DWORD, value = 0x76726148} -- خانەی ٨
        p[7] = {address = b + 36, flags = gg.TYPE_DWORD, value = 0x00747365} -- خانەی ٩
        

        p[8] = {address = b + 40, flags = gg.TYPE_DWORD, value = 0, freeze = true}
        

        p[9] = {address = b + 44, flags = gg.TYPE_DWORD, value = input[1], freeze = true}

        gg.setValues(p)
        gg.addListItems(p)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        gg.clearResults()
    end
end

function tayara()

    gg.clearResults()
    
    gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ ")


gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
    gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
    gg.refineNumber("29", gg.TYPE_DWORD)

    local results = gg.getResults(1)
    if #results == 0 then
        gg.alert("لم يتم العثور على كود الطيران! ❌")
        return 
    end

    local b = results[1].address
    local input = gg.prompt({"اكتب مقدار الوقت للمربع "}, {0}, {"number"})

    if input then
        gg.clearList()
        local p = {}
        p[1] = {address = b + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
        p[2] = {address = b + 16, flags = gg.TYPE_DWORD, value = 0x5F505324}
        p[3] = {address = b + 20, flags = gg.TYPE_DWORD, value = 0x736F6F42}
        p[4] = {address = b + 24, flags = gg.TYPE_DWORD, value = 0x65705374}
        p[5] = {address = b + 28, flags = gg.TYPE_DWORD, value = 0x70556465}
        p[6] = {address = b + 32, flags = gg.TYPE_DWORD, value = 0x00726941}
        p[7] = {address = b + 36, flags = gg.TYPE_DWORD, value = 0x00000000}
        p[8] = {address = b + 40, flags = gg.TYPE_DWORD, value = 0, freeze = true}
        p[9] = {address = b + 44, flags = gg.TYPE_DWORD, value = input[1], freeze = true}

        gg.setValues(p)
        gg.addListItems(p)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        gg.clearResults()
        end
    end
    
    function hewanat()
gg.alert("👨‍🔧 يرجى الانتظار حتى يكتمل البحث 👨‍🔧")
gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
gg.searchNumber("1818848520;107;1150681088::25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("1150681088", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
n = gg.getResultCount()
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address + 0,flags = gg.TYPE_FLOAT,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 160,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 320,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 480,flags = gg.TYPE_DWORD, freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 640,flags = gg.TYPE_DWORD, freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 800,flags = gg.TYPE_DWORD, freeze = true,value = 1}})
end

gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
gg.searchNumber("1701995018;25697;1168687104::25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("1168687104", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
n = gg.getResultCount()
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address + 0,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 128,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 384,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
end

gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearResults()
gg.setVisible(false)

gg.searchNumber("1734829318;1182605312::25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("1182605312", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
n = gg.getResultCount()
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address + 0,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 128,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.addListItems({[1] = {address = jz[i].address + 512,flags = gg.TYPE_DWORD,freeze = true,value = 1}})
gg.alert("⚡ تم بنجاح! وقت جميع الحيوانات الآن صفر ⚡")
gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearList() 
gg.clearResults()
end
end

function SubMenu12() 

    local menu = gg.multiChoice({
    	"╔══════════ 🦋══════════╗\nꕤ     🏘️          تصفير وقت البناء        ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🛩️          تصفير وقت الطائره     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🌱           تصفير وقت زراعة       ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🌱           تصفير وقت  حیوانات     ꕤ\n╚══════════════════════╝",
        "╔══════════ 🦋══════════╗\nꕤ     🔄                رجــــــــــوع               ꕤ\n╚══════════════════════╝",
    
    }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

  
if menu == nil then 
    return 
end


if menu[1] then Binakan() end
if menu[2] then tayara() end
if menu[3] then Agriculture() end
if menu[4] then hewanat() end


if menu[5] then 
    gg.toast("❤️ شكراً للاستخدام")
    return 
end
    end

--[[ ➕ SEROK ARAM LUXURY - FINAL FIXED WITH WARNING ➕ ]]--

local isSearchedZyad = false
local zyadResults = {}

local configZyad = {
    [1] = {name = "الكاش",hex = {1935762184;104;0;0;0;0}},
    [2] = {name = "الليرة الصفراء",hex = {1768907530,29550,0,0,0,0}},
    [3] = {name = "الكاتب الأول",hex = {1635021594,1600484724,1953067639,29285,0,0}},
    [4] = {name = "عملات سباق اليخوت",hex = {1734693396;1130460257;6845281;0;0;0}},
    [5] = {name = "الطاقة لون ازرق",hex = {1886938400;1953064037;1164865385;1735550318;121;0}},
    [6] = {name = " المستوي",hex = {1886938374, 0, 0, 0, 0, 0}}}
function MenuZyadkrdn()
    gg.setVisible(false)
    local menu = gg.multiChoice({

        "╔══════════ 🦋══════════╗\nꕤ     💸               كود الكاش             ꕤ\n╚══════════════════════╝",

        "╔══════════ 🦋══════════╗\nꕤ     🪙             كود الفلوس            ꕤ\n╚══════════════════════╝",

        "╔══════════ 🦋══════════╗\nꕤ     ✍️           كود الكاتب الأول        ꕤ\n╚══════════════════════╝",
        
        "╔══════════ 🦋══════════╗\nꕤ     💎       عملات سباق اليخوت      ꕤ\n╚══════════════════════╝",
        
        "╔══════════ 🦋══════════╗\nꕤ     🗺️          الطاقة لون ازرق          ꕤ\n╚══════════════════════╝",
        
        "╔══════════ 🦋══════════╗\nꕤ     ⭐                    المستوي          ꕤ\n╚══════════════════════╝",

        "╔══════════ 🦋══════════╗\nꕤ     🔄               رجـــــــــوع                ꕤ\n╚══════════════════════╝",

        "╔══════════ 🦋══════════╗\nꕤ     🚪              خـــــــــــروج               ꕤ\n╚══════════════════════╝",

    }, nil,

    "╔══════════════════════╗\n" ..
    "    🦋 🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n" ..
    "╚══════════════════════╝")


    if menu == nil then
        return MenuZyadkrdn()
    end


    -- =========================
    -- رجوع
    -- =========================

    if menu[7] then

        isSearchedZyad = false
        zyadResults = {}

        gg.clearResults()
        gg.clearList()

        gg.toast("🦋 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱 🦋")

        if MainMenu then
            return MainMenu()
        end

        return
    end


    -- =========================
    -- خروج
    -- =========================

    if menu[8] then

        gg.clearList()
        gg.clearResults()

        os.exit()
    end


    -- =========================
    -- دیاریکردنی هەڵبژاردن
    -- =========================

    local anySelected = false

    for i = 1, 6 do
        if menu[i] then
            anySelected = true
            break
        end
    end

    if not anySelected then
        return MenuZyadkrdn()
    end


    -- =========================
    -- گەڕان تەنها یەک جار
    -- دوای هەڵبژاردنی مینۆ
    -- =========================

    if not isSearchedZyad then

        gg.clearResults()

        gg.setRanges(
            gg.REGION_C_ALLOC | gg.REGION_OTHER
        )

        gg.toast("🔍 جاري البحث...")

        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
 gg.refineNumber("29",gg.TYPE_DWORD)

        local count = gg.getResultCount()
        if count == 0 then

            isSearchedZyad = false
            zyadResults = {}

            gg.alert("❌ تأكد من أن اللعبة مرتبطة بجيم جاردن")
  return MenuZyadkrdn()
        end

        zyadResults = gg.getResults(count)

        isSearchedZyad = true
    end


    -- =========================
    -- کۆدی هەڵبژێردراو
    -- =========================

    local input = nil

    -- بۆ کاش و پارەی زەرد تەنها
    -- داواکاری بڕ

    if menu[1] or menu[2] or menu[4] or menu[5] or menu[6]  then

        input = gg.prompt({"اكتب الكمية المطلوبة:"},{"0"},{"number"})

        if input == nil then
            return MenuZyadkrdn()
        end
    end


    local edit = {}
    local freeze = {}

    -- =========================
    -- ڕێگری لە تێکەڵبوونی slot
    -- =========================

    local slotIdx = 1

    for i = 1, 6 do

        if menu[i] and zyadResults[slotIdx] then

            local v = configZyad[i]
            local r = zyadResults[slotIdx]


            -- =========================
            -- +12 = Byte 2 + Freeze
            -- =========================

            table.insert(freeze, {
                address = r.address + 12,
                value = 2,
                flags = gg.TYPE_BYTE,
                freeze = true
            })


            -- =========================
            -- کۆدەکان
            -- =========================

            for j, h in ipairs(v.hex) do

                table.insert(edit, {
                    address = r.address + 12 + (j * 4),
                    value = h,
                    flags = gg.TYPE_DWORD
                })

            end


            -- =========================
            -- کاش / پارەی زەرد
            -- =========================

            if i == 1 or i == 2 or i == 4 or i == 5 or i == 6 then

                table.insert(edit, {
                    address = r.address + 40,
                    value = 0,
                    flags = gg.TYPE_DWORD
                })

                table.insert(edit, {
                    address = r.address + 44,
                    value = tonumber(input[1]),
                    flags = gg.TYPE_DWORD
                })

            end


            slotIdx = slotIdx + 1
        end
    end


    -- =========================
    -- جێبەجێکردن
    -- =========================

    if #edit > 0 then

        gg.setValues(edit)

        if #freeze > 0 then
            gg.addListItems(freeze)
        end

        gg.alert("🙆🏻 تم تبديل هدية 29 بنجاح\n" .. "افتح التصريح واستلم 🙆🏻")

        gg.setVisible(false)

        while not gg.isVisible() do
            gg.sleep(200)
        end

        return MenuZyadkrdn()

    else

        gg.alert( "❌ تأكد من أن اللعبة مرتبطة بجيم جاردن")

        return MenuZyadkrdn()
    end

end




function kurd()
   local menu = gg.multiChoice({
   	"╔══════════ 🌼══════════╗\nꕤ     🚀          زیادة نقاط السباق        ꕤ\n╚══════════════════════╝",
       "╔══════════ 🦋══════════╗\nꕤ     🚪               خـــــــــروج                ꕤ\n╚══════════════════════╝",
    
  }, nil, "╔══════════════════════╗\n    🦋 🅳︎🅸︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎ 🦋\n╚══════════════════════╝")

  if menu == nil then return end
  
  if menu[1] then
    start_auto_hack()
  end
  
  if menu[2] then os.exit() end
end

function start_auto_hack()
  gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
  gg.clearResults()
  
gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
  gg.searchNumber("65538;1952533772::89", gg.TYPE_DWORD)
  

  gg.refineNumber("65538", gg.TYPE_DWORD)
  
  local r = gg.getResults(500)
  local t = {}
  
  for i, v in ipairs(r) do

    t[#t+1] = {address = v.address + 192, flags = gg.TYPE_DWORD, value = 0}
    t[#t+1] = {address = v.address + 196, flags = gg.TYPE_DWORD, value = 0}
    

      local p = gg.getValues({{address = v.address + 328, flags = gg.TYPE_QWORD}})
      local pointer_addr = p[1].value
      

      t[#t+1] = {address = pointer_addr, flags = gg.TYPE_DWORD, value = 0}
      t[#t+1] = {address = pointer_addr + 4, flags = gg.TYPE_DWORD, value = 150}
  end
  

  gg.setValues(t)
  gg.sleep(500)
  
  gg.alert([[
 1️⃣ كن حذراً جداً، هاك المهمات (التاسكات) عليه باند قوي
 2️⃣ بعد إكمال المهمة، اخرج من الكلان فوراً
 3️⃣ بعد إنجاز 40 مهمة، اسحب مهمة واحدة واحذفها لتجنب الباند
 4️⃣ اذكرنا بدعاء خير، حفظك الله ورعاك يا غالي
]], "حسناً")

  kurd()
end




function tayarrrrr()
gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearResults()
gg.setVisible(false)
gg.searchNumber("16842752;1053609165::13", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("16842752", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
n = gg.getResultCount()
jz = gg.getResults(n)
local messageShown = false 
local toastShown = false 
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address - 4 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address - 8 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 0 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 4 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 8 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 12 ,flags = 4,freeze = true,value = 0}})
gg.addListItems({[1] = {address = jz[i].address + 16 ,flags = 4,freeze = true,value = 0}})
 if not messageShown then
 if not toastShown then
gg.alert(" 🚁 اذهب إلى طائرة الهليكوبتر، أرسل طلبًا أو احذفه، وبعدها سيعمل معك بنجاح.  ")
gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
toastShown = true
messageShown = true 
end 
gg.clearResults()
gg.clearList() 
end
end
end

function snduqsuq()
gg.alert("🕵️ يرجى الانتظار حتى يكتمل البحث 🕵️")
gg.toast("🦋🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱🦋")
gg.clearResults()
gg.setVisible(false)
gg.searchNumber('1953063702;1185464320::73', gg.TYPE_DWORD)
gg.refineNumber('1953063702', gg.TYPE_DWORD)
n = gg.getResultCount()
if n == 0 then
gg.alert("❌ لم يتم العثور على المؤشم")
gg.clearResults()
return
end
gg.toast(n)
jz = gg.getResults(n)
local M12 = gg.prompt({"💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮"},{[1]="\n  0 \n"},nil,{'number'})
if M12 == nil or M12[1] == nil then
gg.clearResults()
return
end
for i = 1, n do
gg.addListItems({[1] = {address = jz[i].address - 60, flags = gg.TYPE_DWORD, freeze = true, value = 0} })
gg.addListItems({[1] = {address = jz[i].address - 52, flags = gg.TYPE_DWORD, freeze = true, value = 0}})
gg.addListItems({[1] = {address = jz[i].address - 56, flags = gg.TYPE_DWORD, freeze = true, value = M12[1]}})
end
gg.alert(" 🎅 مبروك! الآن تمت زيادة صناديق التاجر 🎅")
gg.clearResults()
gg.clearList()
end

function snduqmasna3()
gg.alert("✨ قبل البحث، افتح أحد المصانع. ✨")
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.clearResults()
gg.setVisible(false)
gg.searchNumber("3407873;256:41", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("256", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
n = gg.getResultCount()
if n == 0 then
gg.alert("❌ لم يتم العثور على المؤشم")
gg.clearResults()
return
end
jz = gg.getResults(n)
for i = 1, n do
gg.addListItems({
[1] = {address = jz[i].address + 256, flags = gg.TYPE_DWORD, freeze = true, value = 0} })
end
gg.alert("💁‍♂️ افتح الآن جميع الصناديق دون أن ينقص منك أي کاش 💁‍♂️")
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.clearResults()
end

function likat()
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.setVisible(false)
gg.clearResults()
gg.setRanges(gg.REGION_OTHER)
gg.searchNumber("1918978076;6647145:13", gg.TYPE_DWORD)
gg.refineNumber("1918978076", gg.TYPE_DWORD)

local n = gg.getResultCount()
if n == 0 then
    gg.alert("❌ لم يتم العثور على المؤشم")
    return
end

local jz = gg.getResults(n)
for i = 1, n do
    gg.addListItems({
        {address = jz[i].address - 64, flags = gg.TYPE_DWORD, value = 0, freeze = true},
        {address = jz[i].address - 60, flags = gg.TYPE_DWORD, value = 0, freeze = true},
        {address = jz[i].address - 58, flags = gg.TYPE_DWORD, value = 0, freeze = true}
    })
end

gg.clearResults()
gg.toast("💮 🄳🄸🄳🄰🅁🅆🄰🄷🄰🄱💮")
gg.alert("👸 الآن يمكنك زيادة الإعجابات لأصدقائك 👸")
end

local saved_base2 = nil
local saved_copied = nil
local current_menu = "main" -- ئەمە دیاری دەکات ئێستا لە کام مینۆیەیت

function shuunaa()

    if saved_copied == nil or saved_base2 == nil then
        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC)
        

        gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎")
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber("1599099688;1936682818;33;24;23", gg.TYPE_DWORD)
        gg.refineNumber("23", gg.TYPE_DWORD)
        local r1 = gg.getResults(1)
        if #r1 == 0 then gg.alert("لم يتم العثور على الكود الأول") return end
        
        local addr1 = r1[1].address
        saved_copied = gg.getValues({
            {address = addr1 - 8, flags = gg.TYPE_DWORD}, 
            {address = addr1 - 4, flags = gg.TYPE_DWORD}, 
            {address = addr1,     flags = gg.TYPE_DWORD}, 
            {address = addr1 + 4, flags = gg.TYPE_DWORD}, 
            {address = addr1 + 8, flags = gg.TYPE_DWORD}, 
            {address = addr1 + 12, flags = gg.TYPE_DWORD} 
        })


        gg.clearResults()
        gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
        gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
        gg.refineNumber("29", gg.TYPE_DWORD)
        local r2 = gg.getResults(1)
        if #r2 == 0 then gg.alert("لم يتم العثور على الكود الثاني") return end
        saved_base2 = r2[1].address
    end


    local input = gg.prompt({"أدخل رقم المخزن 📊"}, {0}, {"number"})
    
    if input then

        gg.clearList() 
        
        local p = {}
        local b = saved_base2
        
        p[1] = {address = b + 12, flags = gg.TYPE_DWORD, value = 2, freeze = true}
        p[2] = {address = b + 16, flags = gg.TYPE_DWORD, value = saved_copied[1].value, freeze = true}
        p[3] = {address = b + 20, flags = gg.TYPE_DWORD, value = saved_copied[2].value, freeze = true}
        p[4] = {address = b + 24, flags = gg.TYPE_DWORD, value = saved_copied[3].value, freeze = true}
        p[5] = {address = b + 28, flags = gg.TYPE_DWORD, value = saved_copied[4].value, freeze = true}
        p[6] = {address = b + 32, flags = gg.TYPE_DWORD, value = saved_copied[5].value, freeze = true}
        p[7] = {address = b + 36, flags = gg.TYPE_DWORD, value = saved_copied[6].value, freeze = true}
        p[8] = {address = b + 40, flags = gg.TYPE_DWORD, value = 0, freeze = true}
        p[9] = {address = b + 44, flags = gg.TYPE_DWORD, value = input[1], freeze = true}

        gg.addListItems(p)
        gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
        
    end
end

function jalalhh()
    gg.clearResults()
    gg.setRanges( gg.REGION_ANONYMOUS | gg.REGION_C_ALLOC | gg.REGION_OTHER )
    
    
    gg.searchNumber( "1886938386;1113878113;31093;4::25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1 )
    gg.refineNumber( "1886938386", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1 )
    
    local count = gg.getResultsCount()
    if count == 0 then
        gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
        return
    end
    
    local results = gg.getResults(count)
    

    --------------------------------------------------

local choice = gg.choice({
	"╔══════════ 🦋══════════╗\nꕤ     🌺  زيادة المستوي ⇦ (119)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌹  زيادة المستوي ⇦ (156)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌻  زيادة المستوي ⇦ (328)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     💐  زیادة المستوي ⇦ (406)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🏵️  زيادة المستوي ⇦ (590)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌸  زيادة المستوي ⇦ (788)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     💮  زیادة المستوي ⇦ (875)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌼  زيادة المستوي ⇦ (957)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌷  زيادة المستوي ⇦ (981)      ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     🌲 زيادة المستوي ⇦ (1004)    ꕤ\n╚══════════════════════╝",
	"╔══════════ 🦋══════════╗\nꕤ     ↩️        رجــــــــــــــــوع                    ꕤ\n╚══════════════════════╝",
}, nil, "🌟 قائمة ترقية المستويات 🌟")


if choice == nil or choice == 11 then
    return
end

local values = {
    [1] = "100000x4",
    [2] = "200000x4",
    [3] = "1000000x4",
    [4] = "1500000x4",
    [5] = "3000000x4",
    [6] = "5000000x4",
    [7] = "6000000x4",
    [8] = "7000000x4",
    [9] = "7300000x4",
    [10] = "7600000x4"
}

local text = values[choice]


local saved = {}

for i, v in ipairs(results) do
    saved[#saved + 1] = {
        address = v.address + 384,
        flags = gg.TYPE_DWORD
    }
end

if #saved == 0 then
    gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
    return
end


gg.addListItems(saved)

gg.toast("🅳︎??︎??︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎")

gg.loadResults(saved)

local current = gg.getResults(#saved)

if #current == 0 then
    gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
    return
end


gg.editAll(text, gg.TYPE_DWORD)

gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎")
    --------------------------------------------------
    -- بەشی دووەم: وەرگرتن لە Saved List و گۆڕینی عنوان بۆ -16
    --------------------------------------------------
    local saved_items = gg.getListItems()
    if #saved_items == 0 then
        gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
        return
    end

    local minus16 = {}
    for i, v in ipairs(saved_items) do
        minus16[#minus16 + 1] = { address = v.address - 16, flags = gg.TYPE_DWORD }
    end
    
    gg.removeListItems(saved_items)
    gg.addListItems(minus16)
    
    
    gg.loadResults(minus16)
    local current16 = gg.getResults(#minus16)
    if #current16 == 0 then
        gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
        return
    end

    --------------------------------------------------
    -- بەشی سێیەم: گۆڕینی هەموو ئەنجامەکانی ناو لیستی سیڤ بۆ 6
    --------------------------------------------------
    gg.editAll("6", gg.TYPE_DWORD)
    
    gg.alert("💐 تم بنجاح 💐⏳ يرجى الانتظار بضع ثوانٍ حتى يتم فتح جميع الأراضي ⏳")
end


function X2()

gg.setRanges(gg.REGION_C_ALLOC | gg.REGION_OTHER)
gg.searchNumber('65537~65542;1970225964;5;29::457', gg.TYPE_DWORD)
gg.refineNumber("29", gg.TYPE_DWORD)

local results = gg.getResults(gg.getResultsCount())

if #results > 0 then

    local input = gg.prompt(
        {"️‍🔥اكتب السعر لإضافة أيام X2.️‍🔥"},
        {"5000000"}, 
        {"number"}
    )

    if input == nil then
        gg.toast("تم إلغاء العملية.")
        os.exit()
    end


    local user_value = tonumber(input[1]) * 2

    local edit_table = {}
    local freeze_table = {}

    for i, v in ipairs(results) do
 
        table.insert(freeze_table, {
            address = v.address + 12, 
            flags = gg.TYPE_DWORD, 
            value = 2, 
            freeze = true
        })

        local values = {1835619372,1850041445,2037672308,1635214674,1816224882,3299436 }
        
        local current_offset = 16
        for _, val in ipairs(values) do
            table.insert(edit_table, {
                address = v.address + current_offset, 
                flags = gg.TYPE_DWORD, 
                value = val
            })
            current_offset = current_offset + 4
        end

        
        table.insert(edit_table, {
            address = v.address + 40,
            flags = gg.TYPE_DWORD,
            value = 0
        })


        table.insert(edit_table, {
            address = v.address + 44,
            flags = gg.TYPE_DWORD,
            value = user_value
        })
    end

   
    gg.setValues(edit_table)
    gg.addListItems(freeze_table)
    
    gg.alert("🙆🏻تم تبديل هدية 29 بنجاح افتح التصريح واستلم🙆🏻")
else
       gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
end
end


function talbganm()

    gg.clearResults()

    gg.setRanges(
        gg.REGION_C_ALLOC | gg.REGION_OTHER
    )

    gg.toast("🅳︎🅸︎🅳︎🅰︎🆁︎ 🆆︎🅰︎🅷︎🅰︎🅱︎")


    gg.searchNumber(
        "1701345048;1866691681;1702129269;114;0;16842753",
        gg.TYPE_DWORD
    )

   
    gg.refineNumber(
        "16842753",
        gg.TYPE_DWORD
    )

    local results = gg.getResults(1)

    if #results == 0 then
               gg.alert("❌  لم يتم العثور على أي نتائج  ❌")
        return
    end

    local base = results[1].address

    local input = gg.prompt(
        {"اكتب رقم طلب القمح. 🌾📋 "},
        {1000},
        {"number"}
    )

    if input == nil then
        gg.clearResults()
        return
    end

    gg.setValues({
        {
            address = base - 8,
            value = 0,
            flags = gg.TYPE_DWORD
        },
        {
            address = base - 4, 
            value = input[1],
            flags = gg.TYPE_DWORD
        }
    })

    gg.toast("🌾✨ يمكنك الآن طلب القمح من التعاون 🤝🌾")
    gg.clearResults()
end



MainMenu()

while true do
    if gg.isVisible(true) then
        gg.setVisible(false)
        MainMenu()
    end
    gg.sleep(100)
end
