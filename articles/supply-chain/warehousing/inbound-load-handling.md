---
title: Zpracování příchozích nákladů ve skladu pro nákupní objednávky
description: Tento článek popisuje proces zpracování skladu pro vstupní náklady pro nákupní objednávky.
author: Mirzaab
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 43102cb867243a872a5d1df777d8c4102a48e235
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070312"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Zpracování příchozích nákladů ve skladu pro nákupní objednávky

[!include [banner](../includes/banner.md)]

Tento článek popisuje proces zpracování skladu pro vstupní náklady pro nákupní objednávky.

Pro každý příchozí náklad by váš systém již měl obsahovat související prodejní objednávku a může také obsahovat související specifikaci nákladu a/nebo plán přepravy. Další informace o vytváření a správě příchozích nákladů naleznete v tématu [Obchodní proces: plánování přepravy pro příchozí náklady](/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Přehled: jak jsou vytvářeny, registrovány a přijímány příchozí náklady

Následující ilustrace znázorňuje typický tok pro zpracování příchozích nákladů s množstvím nákupních objednávek při jejich dochodu do skladu.

![Proces zpracování příchozího nákladu.](media/inbound-process.png "Proces zpracování příchozího nákladu")

1. **Dodavatel potvrdí nákupní objednávku.**

    Tento proces začíná po zadání nákupní objednávky do systému a jejímu dodání dodavateli, který potvrdí objednávku. Před vytvořením záznamu o příchozím nákladu musí existovat nákupní objednávka. Příchozí náklad však lze vytvořit i v případě, že objednávka nebyla potvrzena. Další informace viz [Schválení a potvrzení nákupních objednávek](../procurement/purchase-order-approval-confirmation.md).

1. **Vytvoří se záznam o příchozím nákladu za účelem plánování doručení a jeho obsahu.**

    Záznam o příchozím nákladu představuje dodávku dodavatele jedné nebo více nákupních objednávek. Je očekáváno, že se náklad dorazí do skladu jako jedna fyzická jednotka přepravy (například nákladní vůz). Záznam o příchozím nákladu se používá pro účely plánování a umožňuje koordinátora logistiky sledovat průběh nákladu od dodavatele. Používá se také k zaznamenání množství řádků objednávky a ke správě postupu prostřednictvím skladových operací, jako je například práce na příchod a zaskladnění. Vytížení lze vytvořit automaticky nebo ručně a mohou být založena buď na nákupní objednávce, nebo na rozšířeném oznámení o dodávce (ASN) od dodavatele. Další informace naleznete v tématu [Vytvoření nebo úprava příchozího nákladu](/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Dodavatel potvrdí expedici nákladu.**

    Když dodavatel odešle břemeno, koordinátor logistiky v přijímajícím skladu potvrdí expedici dodávky. Pokud přijímající společnost používá modul **Správa přepravy**, potvrzení příchozího nákladu spustí další procesy správy nákladu, které jsou přidruženy ke vstupním nákladům. Další informace naleznete v tématu [Potvrzení nákladu pro expedici](/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **K zaznamenání do skladu a pracovníci registrují množství.**

    Když nákladní vozidlo dorazí do skladu, pracovníci skladu zaregistrují množství nákladu. Pokud je použit modul **Řízení skladu**, jsou zaměstnanci registrováni pomocí mobilních zařízení. Další informace naleznete v tématu [Příjemka produktu proti nákupním objednávkám](../procurement/product-receipt-against-purchase-orders.md#registration) a [Registrace množství položek, které přicházejí v rámci příchozího nákladu](#register-item-quantities-arriving).

1. **Zaregistrovaná množství nákladu jsou zaúčtována proti nákupním objednávkám.**

    Po dokončení registrace množství nákladu musí být tato množství příjemka produktu zaúčtována do skladových položek společnosti, aby bylo možné zaznamenat zvýšení fyzického množství na skladě. Další informace naleznete v tématu [příjemka produktu proti nákupním objednávkám - příjemka produktu](../procurement/product-receipt-against-purchase-orders.md#product-receipt) a [Zaúčtování množství produktů proti nákupním objednávkám](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Registrovat množství položek, které přicházejí do příchozího nákladu

Microsoft Dynamics 365 Supply Chain Management podporuje několik provozních přístupů, které zaznamená doručení objednaných produktů. Systém proto můžete nakonfigurovat tak, aby splňoval vaše konkrétní obchodní požadavky. Tento oddíl popisuje postup při registraci příchozích množství položek pomocí mobilního zařízení v případě, že v systému je zapnuta funkce procesů řízení skladu (WMS). Existuje však alternativní tok, který je založen na použití deníku doručení položek místo na mobilní zařízení. Další informace o tomto toku viz [Registrace položek pro položky umožňující procesy řízení skladu s použitím deníku doručení zboží](tasks/register-items-advanced-warehousing.md).

Při prvním doručení příchozího břemene do skladu musí pracovníci skladu registrovat množství položek, které jsou zahrnuty v dodávce. Obvykle používají ruční skenery. Tento Workflow je k dispozici pouze v případě, že v systému existují následující položky:

- **Záznam o příchozím břemenu popisující množství, které je v dodávce očekáváno**

    Dodavatel obvykle potvrdí vstupní záznam o naložení před tím, než je dodávka doručena do skladu. Proto má naložení stav _expedováno._ Pracovníci skladu však mohou také registrovat množství položek pro vytížení, která mají stav _otevřeno_ nebo _přijato_.

- **Nabídka mobilního zařízení konfigurovaná pro podporu příjmu nákladů**

    [Mobilní aplikace Řízení skladu](../warehousing/install-configure-warehouse-management-app.md) pro mobilní zařízení podporuje následující procesy vytváření práce:

    - Přijetí položky nákladu
    - Přijetí a odložení položky nákladu
    - Příjem smíšených registračních značek, kde je pole **Metoda Identifikace řádku zdrojového dokumentu** pro položku nabídky mobilního zařízení nastaveno pro _Přijetí položky nákladu_. Další informace naleznete v tématu [Příjem smíšených registračních značek](mixed-license-plate-receiving.md).
    - Příjem a zaskladnění smíšených registračních značek, kde je pole **Metoda Identifikace řádku zdrojového dokumentu** pro položku nabídky mobilního zařízení nastaveno pro _Přijetí položky nákladu_. Další informace naleznete v tématu [Příjem smíšených registračních značek](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Bez ohledu na proces bude systém generovat práci, která přijme množství zaregistrovaná v přijímacím umístění a umístí je do místa normálního uložení. Při použití procesu _Přijetí a odložení položky nákladu_ či _Přijetí a odložení smíšené registrační značky_, pracovník, který zaregistroval množství nákladu, bude také vyzván zařízením k provedení práce zaskladnění jako součásti úlohy registrace. Naopak, u procesů _Přijetí položky nákladu_ a _Příjem smíšené registrační značky_ se předpokládá, že práce zaskladnění bude provedena odděleně od úlohy registrace.

- **Šablona práce definující práci vyskladnění a uložení pro příchozí náklady**

    Tato položka je propojena s předchozími položkami. Je nutné mít alespoň jednu šablonu práce pro typ pracovního příkazu _Nákupní objednávka_ a musí obsahovat sadu typů práce výdeje/zaskladnění.

Mobilní zařízení pomáhá přijímajícímu pracovníkovi skladu v průběhu registrace množství nákladu. Tento tok vždy zahrnuje následující kroky pro každé ID nákladu:

1. Zadejte ID nákladu.
2. Zadejte číslo položky pro přijaté zboží.
3. Zadejte množství tohoto čísla položky, které je přijato.
4. Zadejte číslo registrační značky pro počáteční skladové místo položky, pokud systém není nastaven na automatické generování tohoto čísla.
5. Klepněte na **OK**.

Poté, co pracovník dokončí tyto kroky, systém provede v příslušných entitách následující aktualizace za předpokladu, že množství na řádku nákupní objednávky bylo doručeno v jednom nákladu a všechna množství nákladu byla zaregistrována:

| Celek | Aktualizace | Poznámka |
|---|---|---|
| Načíst | Pole **Množství vytvořené práce** na řádku nákladu se aktualizuje, aby se zobrazilo registrované množství. | Hodnota **Stavu nákladu** zůstane _Expedováno_ nebo _Otevřeno_, pokud nebylo pro náklad spuštěno žádné potvrzení dodávky. Pokud byl zahájen alespoň jeden řádek práce zaskladnění, změní se na _V procesu_. |
| Skladová transakce nákupní objednávky, pro kterou jsou registrována přidružená množství nákladu |<p>Aktualizují se následující pole:</p><ul><li>Pole <b>Účtenka</b> je nastaveno na <i>Registrovaná</i>.</li><li>Pole <b>Umístění</b> je aktualizováno kódem místa pro přijímací překladiště. (Tento kód je pro každý sklad určen v poli <b>Výchozí skladové místo příjmu</b>.)</li><li>Pole <b>Registrační značka</b> je aktualizováno číslem registrační značky, které bylo zadáno nebo vygenerováno během registrace.</li><li>Pole <b>ID nákladu</b> je aktualizováno číslem nákladu, na které bylo zaregistrováno množství. (Viz poznámka.)</li></ul> | Možnost propojení mezi skladovou transakcí nákupní objednávky a množstvími registrovanými vůči nákladu byla představena ve verzi 10.0.9 jako volitelná funkce, která byla pojmenovaná _Přiřazení skladových transakcí nákupní objednávky k nákladu_. Tato funkce je užitečná zejména pro operační toky, kde je jedna objednávka zakoupeného zboží dodávána jako vícenásobné vytížení, nebo když náklad obsahuje množství pro více nákupních objednávek. |
| Zaskladnění | Práce je vytvořena na základě šablony práce s cílem instruovat pracovníka, aby přesunul zaregistrovaná množství z přijímacího místa do běžného místa uložení. | Volba umístění úložiště je řízena směrnicí umístění PUT. Pokud nebyla definována žádná směrnice skladového místa, místo zaskladnění pro práci je prázdné. |

Mějte na paměti, že pracovníci skladu mohou zaregistrovat příjem nákupní objednávky s jedním nebo více přidruženými náklady bez použití procesu _Příjem položky nákladu_. K dispozici jsou následující metody:

- **Na mobilním zařízení:** použijte procesy _Přijetí řádku nákupní objednávky_ a _Přijetí řádku nákupní objednávky a odložení_. (Pokud pro množství na řádku nákupní objednávky existuje více než jeden náklad, pracovník nemůže použít proces _Přijetí řádku nákupní objednávky_. Místo toho bude pracovník instruován k použití akce zařízení, která je přidružena k procesu _Přijetí položky nákladu_.)
- **V klientovi:** použijte deník doručení položky.
- **V klientovi:** použijte akci **Registrace**, kterou lze otevřít z řádku nákupní objednávky.

> [!NOTE]
> Je-li příjem nákupní objednávky registrován pomocí některé z předchozích metod, není mezi skladovou transakcí nákupní objednávky a nákladem vytvořeno žádné propojení, a to ani v případě, že je zapnuta funkce _Přiřazení skladových transakcí nákupní objednávky k nákladu_. Jedinou výjimkou z tohoto pravidla je použití možnosti **Přijetí řádku nákupní objednávky**, přičemž pouze jeden náklad má pro daný řádek objednávky má jiný stav než _Přijato_.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Zpracovat nesrovnalosti během registrace množství pro příchozí náklad

Pracovníci skladu mohou provádět registraci částečné příjemky na množství nákladu. Každá příjemka množství s částečným nákladem poté vytvoří samostatnou skladovou transakci se stavem příjemky _Registrováno_ pro registrované množství a ID šarže se vztahuje k řádku původní nákupní objednávky.

#### <a name="load-under-receiving"></a>Příjem menšího množství nákladu

Pokud je množství položek menší než množství uvedená v záznamu o nákladu, může při příjmu dojít k potvrzení této nesrovnalosti na základě snížení množství na řádku nákladu tak, aby odpovídalo skutečnému množství, které bylo zaznamenáno a bylo zaregistrováno.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Příjem většího množství nákladu

Navýšení příjmu nastává při přijetí nákladu a množství položky překročí očekávané množství řádku nákladu. V průběhu registrace při registraci můžete určit, zda a do jaké míry je povoleno navýšení příjmu.

Pole **Příjem většího množství nákladu** použijte pro příslušné položky nabídky mobilního zařízení pro řízení toho, co se stane, když se pracovník skladu pokusí zaregistrovat navýšení dodávky. Toto pole je k dispozici pro položky nabídky mobilního zařízení, které používají následující typy procesů vytváření práce:

- Přijetí položky nákladu
- Přijetí a odložení položky nákladu
- Příjem smíšených registračních značek, (když je pole **Metoda Identifikace řádku zdrojového dokumentu** pro položku nabídky mobilního zařízení nastaveno pro _Přijetí položky nákladu_)
- Příjem a zaskladnění smíšených registračních značek, (když je pole **Metoda Identifikace řádku zdrojového dokumentu** pro položku nabídky mobilního zařízení nastaveno pro _Přijetí položky nákladu_)

Následující tabulka vysvětluje dostupné možnosti pro pole **Příjem většího množství nákladu**.

| Hodnota | popis |
|---|---|
| Povolit | Zaměstnanci mohou zaregistrovat příjem množství, které překračují zbývající neregistrované množství pro vybraný náklad, ale pouze v případě, že celkové zaznamenané množství nepřekročí množství řádku nákupní objednávky, které je spojeno s nákladem (po úpravě procenta navýšení dodávky). |
| Blokovat | <p>Pracovníkům nemohou registrovat příjem množství větších, než je zbývající neregistrované množství pro vybraný náklad (upraveno pro procento navýšení dodávky). Pracovník, který se pokouší zaregistrovat příjemky, obdrží chybu a nebude moci pokračovat, dokud nezaregistruje množství, které je rovno nebo menší než zbývající neregistrované množství.</p><p>Ve výchozím nastavení je hodnota procenta navýšení dodávky zkopírována z přidruženého řádku nákupní objednávky. Pokud je pole <b>Příjem většího množství nákladu</b> nastaveno na <i>Blokovat</i>, systém použije procentuální hodnotu přecenění k výpočtu celkového množství, které může být zaregistrováno pro řádek nákladu. Tato hodnota však může být pro jednotlivé náklady podle potřeby přepsána. Toto chování se stává relevantním při příjmu toků v případě, že některá nebo všechna nadbytečná množství představující procento navýšení dodávky řádku objednávky je rozložena neúměrně k více nákladům. Následuje ukázkový scénář:</p><ul><li>Pro jeden řádek nákupní objednávky existuje více nákladů.</li><li>Řádek nákupní objednávky má procento navýšení dodávky, které je větší než 0 (nula).</li><li>Množství již byla registrována proti jednomu nebo více nákladům, aniž by bylo nutné brát v úvahu procento navýšení dodávky.</li><li>Vyšší množství dodávky dorazí v posledním nákladu.</li></ul><p>V tomto scénáři lze mobilní zařízení použít k zaregistrování nadbytečného množství pro poslední náklad pouze v případě, že vedoucí skladu zvýší procento navýšení dodávky pro příslušný řádek nákladu z výchozí hodnoty na dostatečně velkou hodnotu, aby bylo možné registrovat úplné navýšení dodávky při konečném nákladu.</p> |
| Blokovat pouze pro uzavřené náklady | Zaměstnanci mohou přebírat vyšší množství řádků nákladu pro otevřené náklady, ale ne pro náklady, která mají stav _Přijato_. |

> [!NOTE]
> Výchozí hodnota pole **Příjem většího množství nákladu** je _Povoleno_. Při použití této hodnoty se chování shoduje se standardním chováním, které bylo k dispozici před zavedením funkce _Příjem většího množství nákladu_ ve verzi 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Zaskladnit registrovaná množství

Když je registrace dokončena na mobilním zařízení, akce _Registrace příjemky množství_ aktualizuje záznamy zásob a skladů s cílem označit, že množství jsou nyní v přijímacím skladovém místě a k dispozici pro rezervaci. Skladové operace společnosti však obvykle vyžadují, aby byla množství přesunuta z přijímacího překladiště do běžného skladového místa, aby mohlo dojít k následným procesům výdeje. Pokyny pro zaskladnění jsou zachyceny v práci zaskladnění, která je automaticky generována při registraci příchozího nákladu jako přijatého.

Když pracovník skladu dokončí práci zaskladnění, systém zaznamená a bude sledovat výsledek aktualizací několika entit, které jsou shrnuty v následující tabulce.

| Celek | Aktualizace | Poznámka |
|---|---|---|
| Načíst | <p>Aktualizují se následující pole:</p><ul><li>Hodnota <b>Stav nákladu</b> se změnila na <i>zpracovává se</i>.</li><li>Hodnota <b>Stav práce</b> je změněna na <i>100,00% práce dokončeno</i>.</li></ul> | Hodnota **Stav nákladu** se změnila na _Zpracovává se_, když pracovník zahájí úlohu zaskladnění pro alespoň jeden řádek zaskladnění. |
| Skladové transakce práce, pro které bylo zaskladněno související množství | Pole **Příjemka** a **Umístění** a další související pole jsou aktualizována tak, aby odrážela pohyb z přijímacího místa do skladového místa. | Hodnota **Stav příjmu** skladové transakce nákupní objednávky zůstane _Zaregistrováno_. |
| Zaskladnění | Hodnota **Stv práce** se změnila na _Uzavřeno_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Zaregistrovaná množství nákladu zaúčtována proti nákupním objednávkám

Po registraci vstupních množství produktů v systému budou tyto hodnoty k dispozici pro rezervaci v souvislosti s prodejem a jinými výstupními a interními operacemi. Systém však ještě neprovede aktualizaci skladových (dočasných) účtů. Tato aktualizace může nastat pouze v případě, že tým operací zaúčtuje registrované příjemky produktu.

Chcete-li otevřít stránku, na níž mohou být zaúčtovány příjemky produktu, členové provozního týmu mohou sledovat _jeden_ z následujících kroků:

- Otevřete příslušný záznam nákladu a poté vyberte akci **Příjemka produktu**.
- Přejděte na **Řízení skladu \> Periodické úlohy \> Aktualizovat příjemky produktů** a pak v poli **ID nákladu** určete náklad k zaúčtování.
- Otevřete příslušnou nákupní objednávku a poté vyberte akci **Příjemka produktu**.
- Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Příjem produktů \> Úloha zaúčtování příjemky produktu**.

Akce **Příjemka produktu**, která je k dispozici na stránce **Náklad** (a na ekvivalentní stránce pro úlohu aktualizace **Aktualizovat příjemky produktů**), může aktualizovat množství příjemky produktu pouze u množství na nákupních objednávkách, které mají stav _Registrováno_. Akce **Příjemka produktu**, která je k dispozici na stránce **Nákupní objednávka**, však může zahrnovat množství ve stavech zpracování (_Objednáno_ a _Registrováno_). Může také určovat rozsah zaúčtování příjemky produktu pomocí dodatečných parametrů, jako je _Množství nynějšího příjmu_ a _Registrované množství a služby_.

Pouze objednávky, které mají stav _Potvrzeno_, mohou být zaúčtovány. U nepotvrzených nákupních objednávek se akce **Příjemka produktu** zobrazí jako Není k dispozici.

### <a name="post-registered-quantities-from-the-load-page"></a>Zaúčtovat zaregistrovaná množství ze stránky Náklad

Příjemka produktu – chcete-li zaúčtovat zaregistrovaná množství ze stránky **Náklad**, musí být zavedeny následující předpoklady:

- Náklad musí mít alespoň jednu jednotku množství, která má stav _Registrováno_.
- Stav nákladu musí být _Expedován_.
- Nákupní objednávka, která je přidružená k nákladu, musí mít stav _Potvrzeno_.

> [!NOTE]
> Pokud stav nakládky není nastaven na _Expedováno_, systém před spuštěním aktualizace příjemky produktu ověření automaticky potvrdí. (Stav nakládky je nastaven na _Expedováno_ při zaregistrování příchozí dodávky uživatelem.)

Příjemka produktu – chcete-li zaúčtovat registrace doručení, které jsou přidruženy k vybranému nákladu, pracovník vybere akci **Příjemka produktu** na stránce **Náklad**. Otevřená stránka obsahuje následující klíčové údaje:

- V poli **Množství** v části **Parametry** na kartě **Nastavení** se zobrazí _registrované množství_. V tomto poli nejsou k dispozici žádné další možnosti.
- V mřížce na pevné záložce **Přehled** jsou uvedeny všechny nákupní objednávky zahrnuté ve vybraném nákladu.
- V mřížce na pevné záložce **Řádky** jsou uvedeny všechny řádky objednávky, které mají registrované množství.

> [!NOTE]
> Množství pro řádky objednávky, které se zobrazí na kartě **Řádek**, jsou vypočítána různě v závislosti na tom, zda je k dispozici a zapnutá funkce _Povolit více příjemek produktů na náklad_ ve vaší verzi modulu Supply Chain Management.
>
> | Verze | Výpočet |
> |---|---|
> | Verze před verzí 10.0.10 a novější verze, kde není zapnuta funkce _Povolit více příjemek produktů na náklad_ | Množství na řádku je součtem všech registrovaných množství _pro daný řádek nákupní objednávky_ bez ohledu na to, zda byla registrace provedena přes více nákladů, nezávisle na nákladu, z mobilního zařízení nebo klienta. |
> | Verze 10.0.10 a novější verze, kde je zapnuta funkce _Povolit více příjemek produktů na náklad_ | Množství na řádku je součtem všech registrovaných množství _záznamu nákladu_, ze kterého byla zahájena akce **Zaúčtování příjemky produktu** . |

Když uživatel vybere **OK** k potvrzení zaúčtování příjemky produktu, systém provede následující aktualizace příslušných entit.

| Celek | Aktualizace |
|---|---|
| Skladová transakce nákupní objednávky, pro kterou bylo zahrnuto množství řádků v rozsahu zaúčtování | <p>Jsou aktualizována následující pole (poznámka: existuje také více aktualizací):</p><ul><li>Pole <b>Účtenka</b> je nastaveno na <i>Obdrženo</i>.</li><li>Pole <b>Fyzické datum</b> je aktualizováno datem zaúčtování.</li></ul> |
| Náklad, ze kterého uživatel zaúčtoval příjemku produktu | Aktualizace nákladů budou záviset na použité verzi a na nastavení pole **Povolit více příjemek produktů na náklad**. Pravidla jsou popsána v tabulce, která se zobrazí dále v této části. |

Pole **Povolit více příjemek produktů na náklad** umožní společnostem zvolit zásadu příjmu pro nákladu. V závislosti na provozních tocích se mohou společnosti rozhodnout povolit nebo zakázat více zaúčtování příjemek produktů pro stejný náklad. Doporučujeme, aby vedoucí logistiky nastavil pole **Povolit více příjemek produktů na náklad** na jednu z následujících hodnot:

- **Ne** – tuto hodnotu vyberte, pokud pracovník příjmu v rámci skladu vždy zaregistruje všechna objednaná množství, která byla doručena při každém nákladu za určené časové období. Nejsou-li zaregistrována žádná množství nákladů, systém předpokládá, že nebyly přijaty nebo nebyly v nákladu, a proto by neměly být považovány za součást nákladu. Zaúčtování příjemky produktu, které je spuštěno z nákladu, používá stejný předpoklad. Kromě příjemky produktu – aktualizací všech registrovaných množství (její hlavní funkce) deklarujete, že náklad je dokončen a uzavřen pro další zpracování. V takovém případě budou všechna množství na řádku nákladu automaticky aktualizována na registrované množství, řádky nákladu bez registrovaného množství budou odstraněny a stav nákladu se změní na _Přijato_.
- **Ano** – tuto hodnotu vyberte v případě, že pracovník příjmu skladu potřebuje k evidenci všech množství, která byla doručena, ale do té doby je nutné zaznamenat příjemku produktu – zaúčtovat množství, která již byla zaregistrována. V takovém případě vedoucí logistiky bude chtít ponechat otevřený náklad i po spuštění zaúčtování příjemky produktu, takže zbývající množství nákladu může být registrováno a příjemka produktu aktualizována do hlavní knihy průběžně.
- **Dotázat se** - tuto hodnotu vyberte v případě, že jsou smíšené způsoby příjmu nákladu a při každém spuštění zaúčtování příjemky produktu je požadováno rozhodnutí.

V následující tabulce jsou shrnuty účinky nastavení **Povolit více příjemek produktů na náklad**.

| Povolit více příjemek produktů na jeden náklad | Množství nákladu | Stav nákladu | Poznámka |
|---|---|---|---|
| Pokud toto pole není k dispozici (verze před 10.0.10) | <p>Množství nákladu je nastaveno tak, aby se rovnalo zaregistrovanému množství.</p><p>Pokud je množství nákladu aktualizováno na 0 (nula), což znamená, že nebyla provedena žádná registrace, řádek nákladu bude odstraněn.</p><p>Pokud pro náklad nejsou k dispozici žádné řádky pro čtení, dojde k jeho odstranění.</p> | _Přijato_ | Existuje-li pro zaregistrované množství řádku objednávky více nákladů, aktualizuje se na _přijato_ pouze stav nákladu, ze kterého byla zaúčtována příjemka. |
| Ne | <p>Množství nákladu je nastaveno tak, aby se rovnalo zaregistrovanému množství, které je přidruženo k ID nákladu.</p><p>Pokud není pro skladovou transakci zaznamenáno ID nákladu, chování odpovídá chování ve verzích před 10.0.10.</p> | _Přijato_ | |
| Ano | Žádné aktualizace | _Přijato_, pokud je celkové zaregistrované množství nákladu rovno nebo větší než množství nákladu | |
| Ano | Žádné aktualizace | _Odesláno_ nebo _Zpracovává se_, pokud je celkové zaregistrované množství nákladu menší než množství nákladu | |

Po nastavení pole **Stav nákladu** na _Přijato_ již nelze pro daný náklad provést další zaúčtování příjemky produktu. Pracovník však může zaregistrovat zbývající množství objednávky proti přijatému nákladu za následujících podmínek. (Další informace naleznete v oddílu [Příjem většího množství nákladu](#load-over-receiving) dříve v tomto článku.)

- Verze Supply Chain Management je starší než verze 10.0.11.
- Pokud je zapnuta funkce _Příjem většího množství nákladu_ a **Množství řádku nákladu větší, než příjemka** v položce nabídky mobilního zařízení pro akci přijetí položky nákladů je nastaveno na _Povolit_.

Příjemka produktu – pro zaúčtování dalších registrovaných množství do nákladu, které mají stav _přijato_, musí uživatel spustit akci zaúčtování z přidružené nákupní objednávky.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Zaúčtovat zaregistrovaná množství ze stránky Nákupní objednávka

Příjemka produktu – pro zaúčtování registrovaných množství ze stránky **Nákupní objednávka** uživatel před vybráním akce **Příjemka produktu** dokončí následující úkoly:

- Nastaví pole **Množství** v části **Parametry** na kartě **Nastavení** na _Registrované množství_.
- Do pole **Příjemka produktu** zadejte čísla nákupních objednávek, které jsou zahrnuty do zaúčtování.

> [!NOTE]
> Množství na řádku, které bude zahrnuto do rozsahu zaúčtování, je součtem všech registrovaných množství pro daný řádek nákupní objednávky bez ohledu na to, zda byla registrace množství provedena přes více nákladů, nezávisle na nákladu, z mobilního zařízení nebo klienta. Stejné pravidlo platí v případě, že zaúčtování příjemky produktu je spuštěno z nákladu, pokud pole **Povolit více příjemek produktů na jeden náklad** buď není dostupné, nebo není povoleno.

Když uživatel vybere **OK** k potvrzení zaúčtování příjemky produktu, systém provede následující aktualizace příslušných entit.

| Celek | Aktualizace |
|---|---|
| Skladová transakce nákupní objednávky, pro kterou bylo zahrnuto množství řádků v rozsahu zaúčtování | <p>Jsou aktualizována následující pole (poznámka: existuje také více aktualizací):</p><ul><li>Pole <b>Účtenka</b> je nastaveno na <i>Obdrženo</i>.</li><li>Pole <b>Fyzické datum</b> je aktualizováno datem acte zaúčtování příjemky produktu.</li></ul> |
| Načíst | Aktualizace načtených položek závisejí na tom, zda je k dispozici a povoleno pole **Povolit více příjemek produktů na náklad**. Pravidla jsou popsána v následující tabulce. |

V následující tabulce jsou shrnuty účinky nastavení **Povolit více příjemek produktů na náklad**.

| Povolit více přijetí produktu na vytížení | Množství nákladu | Stav nákladu | Poznámka |
|---|---|---|---|
| Pokud je toto pole zakázáno nebo není k dispozici (verze před 10.0.10) | Žádné aktualizace | Nebyly provedeny žádné aktualizace. (Stav zůstane _Otevřeno_, _Odesláno_ nebo _Zpracovává se_.) | Vzhledem k tomu, že zaúčtování příjemky produktu je zahájeno z nákupní objednávky, logika aktualizace neobsahuje informace o přidružení mezi registrovanými množstvími v rámci rozsahu a nákladů, na které byla registrace zaznamenána. Proto nemůže vybrat náklad pro aktualizaci stavu. |
| Povoleno | Žádné aktualizace | <p>Nastane jedna z následujících akcí:</p><ul><li>Stav se změní na <i>Přijato</i>, pokud celková přijatá a zakoupená množství skladových transakcí nákupní objednávky je větší nebo rovna množství nákladu, ke kterému jsou přidružena.</li><li>Stav zůstává <i>Otevřeno</i>, <i>Odesláno</i> nebo <i>Zpracovává se</i>, pokud není pro všechny řádky nákaldu splněna předchozí podmínka.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Vyberte možnost zaúčtování příjemky produktu pro vaše logistické operace

Jak bylo uvedeno dříve, systém nabídne dvě možnosti zaúčtování příjemky produktu. K možnostem lze přistupovat v následujících místech:

- Na stránce **Náklad** nebo v nabídce **Řízení skladu \> Periodické úkoly** jako úloha aktualizace
- Na stránce **Nákupní objednávka** nebo v nabídce **Zásobování a zdroje \> Nákupní objednávky \> Příjem produktů** jako úloha aktualizace

Společnosti, které používají náklady pro plánování a správu přepravy a zpracování příchozích objednávek, mohou použít následující funkce, které jsou navrženy pro práci s náklady:

- Akce **Přijetí položky nákladu** v mobilních zařízeních skladu, aby se registrovalo dodání množství produktu proti nákladu
- Akce **Zaúčtování příjemky produktu** zahájené z nákladu pro aktualizaci hlavní knihy zásob

> [!NOTE]
> Další registrace množství a zaúčtování příjemek produktu lze použít pro podporu odpovídajících vstupních provozních procesů. Pokud je použijete však zaměnitelně pomocí nebo namísto vyhrazených funkcí zaměřených na náklad, může dojít ke zhoršení přesnosti dat o nákladu a tedy i plynulosti toků správy nákladu.

## <a name="example-scenarios"></a>Ukázkové scénáře

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Příprava systému ke spuštění ukázkových scénářů

Chcete-li pracovat se vzorovými scénáři popsanými v této části, musíte nejprve zkontrolovat, zda jsou v systému zapnuty všechny požadované funkce. Požadovaná ukázková data musí být také k dispozici v systému.

#### <a name="turn-on-the-required-features"></a>Zapnutí požadovaných funkcí

Tyto scénáře vyžadují funkci _Více zaúčtování příjemek produktů na náklad_ a její požadovanou funkci. Správci mohou tyto funkce zapnout provedením následujících kroků.

1. Otevřete pracovní prostor **Správa funkcí**. (Podrobné informace o tom, jak najít a použít tento pracovní prostor naleznete v tématu [Správa funkcí – přehled](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)funkcí – přehled.)

1. Ujistěte se, že je zapnutá funkce _Přiřazení skladových transakcí nákupní objednávky k nákladu_. Od Supply Chain Management verze 10.0.21 je tato funkce povinná, takže je ve výchozím nastavení zapnutá a nelze ji znovu vypnout. Ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) je však tato funkce uvedena následovně:

    - **Modul:** _Řízení skladu_
    - **Název funkce:** _Přiřazení skladových transakcí nákupní objednávky k nákladu_

1. Zapněte funkci _Více zaúčtování příjemek produktů na náklad_, která je uvedeno následujícím způsobem:

    - **Modul:** _Řízení skladu_
    - **Název funkce:** _Více zaúčtování příjemek produktů na náklad_

#### <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li s těmito scénáři pracovat pomocí zadaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data. Dříve než začnete, musíte také vybrat právnickou osobu **USMF**.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Přidání položky nabídky pro příjem položek nákladu při použití mobilního zařízení

Před tím, než pracovníci příjmu skladu mohou použít mobilní zařízení k registraci příchozích zásob, které jsou spojeny s nákladem, je nutné pro tento účel vytvořit položku nabídky mobilního zařízení.

V tomto oddílu vytvoříte položku nabídky pro mobilní zařízení a přidáte ji do existující nabídky. Pracovník skladu pak může vybrat položku nabídky v mobilní aplikaci Řízení skladu.

1. Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení** a ujistěte se, že nabídka mobilního zařízení obsahuje položku nabídky s následujícími nastaveními:

    - **Režim:** _Práce_
    - **Proces vytváření práce:** _Příjem položek nákladu_
    - **Generovat registrační značky:** _Ano_

    Všechna ostatní nastavení lze ponechat ve výchozích hodnotách.

    ![Nastavení položky nabídky mobilních zařízení.](media/inbound-mobile-menu-items.png "Nastavení položky nabídky mobilních zařízení")

    Další informace o nastavení položek nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).

2. Po dokončení nastavení položky nabídky přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení** a přidejte ji do struktury nabídky vašich mobilních zařízení.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Příklad scénáře 1: registrace nákladu, kde některé položky chybí

Tento scénář ukazuje, jak registrovat množství pro příchozí náklad, pokud neobsahuje všechna očekávaná množství. Poté ukazuje, jak zaúčtovat příjemku produktu pro nákupní objednávku.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Vytvořte náklad pro plán příjmu nákupní objednávky

V tomto postupu můžete ručně vytvořit nákupní objednávku a související náklad. Poté aktualizujete náklad, aby se simulovalo, že byl dodán dodavatelem (který aktualizuje stav nákladu). Plánovači skladu pak mohou vyfiltrovat náklady dle **Stavu nákladu** pro nalezení očekávaných příchozích nákladů.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vytvořit nákupní objednávku** nastavte pole **Účet dodavatele** na _1001_.
1. Vyberte **OK** k zavření dialogového a vytvoření nákupní objednávky.
1. Nová nákupní objednávka již obsahuje řádek v **Řádcích nákupní objednávky**. Pro tento řádek nastavte následující hodnoty:

    - **Číslo položky:** _A0001_
    - **Sklad:** _24_
    - **Množství:** _10_

1. V podokně akcí na kartě **Nákup** vyberte **Akce \> Potvrdit**. Stav objednávky je nyní _Potvrzeno_.
1. V podokně akcí na kartě **Sklad** vyberte **Akce \> Pracovní plocha plánování vytížení**.
1. Na stránce **Pracovní plocha plánování vytížení** v podokně akcí na kartě **Nabídka a poptávka** vyberte možnost **Přidat \> Do nového nákladu**.
1. V dialogovém okně **Přiřazení šablony nákladu** nastavte pole **ID šablony nákladu** na _20' Container_.
1. Vyberte **OK** k zavření dialogového a návratu do pracovní plochy.
1. V části **Náklady** vyberte položku **ID nákladu** a otevřete nově vytvořený náklad.
1. Zkontrolujte záhlaví a podrobnosti řádku nákladu a všimněte si následujících bodů:

    - Na pevné záložce **Náklad** je pole **Stav nákladu** nastaveno na _Otevřeno_.
    - V části **Řádky nákladu** je k dispozici jediný řádek, ve kterém je pole **Množství** nastaveno na _10_ a pole **Množství vytvořené práce** je nastaveno _0_ (nula).

    ![Podrobnosti o nákladu.](media/inbound-load-details.png "Podrobnosti o nákladu")

1. V podokně akcí na kartě **Expedovat a přijmout** vyberte **Potvrdit \> Příchozí dodávka**. Povšimněte si, že **Stav nákladu** se změnil na _Expedováno_.
1. Poznamenejte si hodnotu **ID nákladu**, aby jej bylo možné použít v dalším postupu.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Zaregistrujte příjem množství, která byla doručena do nákladu

Když je do skladu doručen náklad, pracovník příjmu zaregistruje množství nákladu v mobilním zařízení.

1. Pomocí mobilního zařízení se přihlaste ke skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla _24_ ID uživatele a _1_ jako heslo.)
1. Vyberte položku nabídky _Přijetí položky nákladu_, kterou jste vytvořili pro tento scénář.
1. Chcete-li zadat následující hodnoty, postupujte podle instrukcí pro zadávání dat na obrazovce. (Pořadí se může lišit v závislosti na mobilním zařízení nebo emulátoru, které používáte.)

    - **Náklad** – zadejte ID nákladu, které jste vytvořili v předchozím postupu.
    - **Položka** – zadejte _A0001_, což je položka, která je pro toto náklad očekávána.
    - **Množství** – zadejte _9_ jako skutečné množství, které je k dispozici v nákladu. Povšimněte si, že toto množství je menší než očekávané množství.

1. Pokračovat v procházení pracovního postupu, ponechat všechna ostatní pole prázdná nebo nastavit na výchozí hodnoty, dokud vám zařízení neinformuje o dokončení práce.

Úkol přijetí nákladu je nyní dokončen a pracovník příjmu se může přesunout na následující úkol. Přijímající pracovník však nakonec zkontroluje záznam o nákladu a bude moci zjistit, že přijaté množství je menší než očekávané množství. Poté vyplní následující postup pomocí webového klienta.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V seznamu najděte náklad, které jste právě přijali. (Je možné, že bude nutné zaškrtnout políčko **Zobrazit uzavřené**, chcete-li zahrnout vstupní stavy se stavem nákladu _Expedováno_.) Poté výběrem odkazu ve sloupci **ID nákladu** otevřete požadovaný náklad.
1. V záznamu nákladu si všimněte, že hodnota **Stav nákladu** zůstane _Expedováno_, ale hodnota **Množství vytvořené práce** na řádku nákladu se změnila na _9_.
1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V seznamu najděte právě přijatý nákup a poté výběrem odkazu ve sloupci **Nákupní objednávky** otevřete objednávku.
\
1. Na pevné záložce **Řádky nákupní objednávky** vyberte **Zásoby \> Zobrazit \> Transakce**.
1. Zkontrolujte podrobnosti o dvou transakcích nákupní objednávky. (Bude pravděpodobně nutné přizpůsobit stránku **Skladové transakce**, chcete-li zobrazit pole **ID nákladu** v mřížce.) Měly by se zobrazit dvě transakce:

    - Transakce s příjemkou ve stavu _registrováno_ představuje registrační množství _9_, které bylo spuštěno proti konkrétnímu nákladu pomocí mobilního zařízení. **ID nákladu** je přidruženo k dané transakci.
    - Transakce, která má příjemku ve stavu _Objednáno_, představuje zbývající neregistrované množství řádku objednávky _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Příjemka produktu - zaúčtovat registrovaná množství nákladu proti nákupním objednávkám

V tomto postupu zaúčtujete příjemku produktu – zásoby, které jste zaregistrovali pro náklad. V důsledku toho budou přijaté zásoby a související náklady přidány do hlavní knihy společnosti.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V seznamu najděte náklad, které jste přijali. (Je možné, že bude nutné zaškrtnout políčko **Zobrazit uzavřené**, chcete-li zahrnout vstupní stavy se stavem nákladu _Expedováno_.) Poté výběrem odkazu ve sloupci **ID nákladu** otevřete požadovaný náklad.
1. V podokně akcí na kartě **Expedovat a přijmout** vyberte **Přijmout \> Příjemka produktu**. Vyberte **Ano** po zobrazení výzvy k potvrzení výběru.
1. V dialogovém okně **Zaúčtování příjemky produktu** na pevné záložce **Řádky** prozkoumejte mřížku. Měl by se zobrazit řádek nákupní objednávky, pro který bylo u vybraného nákupu zaregistrováno množství.

    > [!NOTE]
    > Ve verzích, kde není k dispozici funkce _Více zaúčtování příjemek produktů na náklad_ nebo není povolena, výchozí množství zobrazené v mřížce **Řádky nákladu** bude celkové množství, které bylo zaregistrováno napříč všemi náklady, které jsou přiřazeny k řádku nákupní objednávky.

1. Na pevné záložce **Přehled** prozkoumejte pole **Příjemka produktu** v mřížce. Všimněte si, že je nastaveno na číslo, které obsahuje ID vybraného nákladu.
1. Výběrem **OK** zaúčtujte příjemku produktu a zavřete dialogové okno **Zaúčtování příjemky produktu**.
1. Vrátíte se k podrobnostem o nákladu. Mějte na paměti následující body:

    - Pole **Stav nákladu** je nyní nastaveno na _přijato_.
    - V řádku nákladu se hodnota **Množství** pro náklad změnila z _10_ na _9_ kusů tak, aby souhlasila s registrovaným množstvím, ale hodnota **Množství vytvořené práce** zůstává _9_.

Pokud nákupní tým neočekává, že dodavatel doručí zbývající množství objednávky 1, může objednávku uzavřít aktualizací zůstatku řádku dodání na _0_. Pokud však brzy zjistíte, že chybějící část došla k původnímu břemenu, pracovníci skladu mohou provést některou z následujících akcí:

- Zaregistrujte množství oproti stejnému nákladu. V tomto případě bude pole **Stav nákladu** obnoveno na hodnotu _Expedováno_ a **Množství vytvořené práce** bude aktualizováno na _10_. Tato volba je k dispozici pouze v následujících situacích:

    - Funkce _Příjem většího množství nákladu_ není k dispozici nebo není povolena.
    - Funkce _Příjem většího množství nákladus_ je k dispozici a povolena a pole **Množství řádku nákladu větší, než příjemka** je nastaveno na _Povolit_.

- Přidejte množství do nového nebo stávajícího nákladu a zpracujte jej obvyklým způsobem.
- Registrace a přijetí množství způsobem, který nezahrnuje zpracování nákladu.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Příklad scénáře 2: registrace množství, která přijíždí v několik apříchozích nákladech, pokud některé položky chybí

V tomto scénáři bude příchozí dodávka, která souvisí s jedním řádkem nákupní objednávky, rozdělena do dvou nákladů. Řádek nákupní objednávky může být například rozdělen do více nákladů kvůli fyzickým omezením vytížení hmotnosti nebo objemu.

Tento scénář také ukazuje, jak zpracovat více zaúčtování příjemky produktu pro stejný náklad. Zaznamenáte množství, která budou přijata na více příchozích nákladech, ale tato množství se neshodují s očekávaným množstvím. Aktualizace nákladů, ke kterým dochází prostřednictvím zaúčtování příjemky produktu, budou provedeny vícekrát pro stejné náklady.

#### <a name="set-up-load-receiving-policies"></a>Nastavit zásady příjmu nákladu

V tomto postupu povolíte více zaúčtování příjemek produktů ze stejného nákladu.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Náklady** nastavte pole **Povolit více příjemek produktů na jeden náklad** na _Ano_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Vytvořte dva náklady pro plán příjmu nákupní objednávky

V tomto postupu můžete ručně vytvořit nákupní objednávku a dva náklady. Poté ručně aktualizujete každý náklad, aby se simulovalo, že byl dodán dodavatelem (který aktualizuje stav nákladu). Plánovači skladu pak mohou vyfiltrovat náklady dle **Stavu nákladu** pro nalezení očekávaných příchozích nákladů.

Dále se naučíte, jak nastavit řádek nákupní objednávky, abyste mohli obdržet množství o 20 procent větší, než je množství zadané pro daný řádek.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Zvolte **Nové**.
1. Na pevné záložce **Dodavatel** nastavte pole **Účet dodavatele** na _1001_ a pak vyberte **OK**.
1. Bude otevřena nová nákupní objednávka a bude obsahovat prázdný řádek v mřížce **Řádky nákupní objednávky**. Pro tento řádek objednávky nastavte následující hodnoty:

    - **Číslo položky:** _A0001_
    - **Sklad:** _24_
    - **Množství:** _10_

1. Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** nastavte pole **Navýšení dodávky** na _20_.
1. V podokně akcí na kartě **Nákup** vyberte **Akce \> Potvrdit**. Stav objednávky je nyní _Potvrzeno_.
1. V podokně akcí na kartě **Sklad** vyberte **Akce \> Pracovní plocha plánování vytížení**.
1. Na stránce **Pracovní plocha plánování vytížení** v podokně akcí na kartě **Nabídka a poptávka** vyberte možnost **Přidat \> Do nového nákladu**.
1. V dialogovém okně **Přiřazení šablony nákladu** nastavte pole **ID šablony nákladu** na _20' Container_. Na kartě **Podrobnosti** změňte hodnotu **Množství** z _10_ na _5_ a částečně tak přidejte množství řádku nákupní objednávky.
1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno.
1. Zopakováním kroků 8 až 10 vytvořte druhý náklad. Tentokrát by mělo být pole **Množství** již nastaveno na _5_.
1. Na stránce **Pracovní plocha plánování nákladu** v mřížce **Náklady** vyberte hodnotu **ID nákladu** pro první vytvořený náklad. Zobrazí se stránka **Podrobnosti o nákladu** a zobrazí se vybraný náklad. Postupujte následovně:

    1. V podokně akcí na kartě **Expedovat a přijmout** vyberte **Potvrdit \> Příchozí dodávka**.
    1. Povšimněte si, že hodnota **Stav nákladu** se změnila na _Expedováno_.
    1. Chcete-li se vrátit na stránku **Pracovní plocha plánování nákladu**, vyberte tlačítko Zavřít.

1. Opakujte předchozí krok pro druhý náklad, které jste vytvořili.
1. Poznamenejte si dvě hodnoty **ID nákladu**, které se zobrazí v mřížce **Náklad**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Registrovat částečný příjem množství, které bylo doručeno v prvním nákladu a zaúčtovat zaregistrovaná množství nákladu

Když jsou do skladu doručeny náklady, pracovník příjmu zaregistruje množství nákladu v mobilním zařízení. Registrované zásoby, které jsou spojeny s nákladem, se pak aktualizují podle nákladů hlavní knihy společnosti zaúčtováním příjemky produktu nákupní objednávky na základě nákladu.

Tento postup ukazuje, jak bude přijímající pracovník registrovat množství nákladu v mobilním zařízení.

1. Pomocí mobilního zařízení se přihlaste ke skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla _24_ ID uživatele a _1_ jako heslo.)
1. Vyberte položku nabídky _Přijetí položky nákladu_, kterou jste vytvořili pro tento scénář.
1. Chcete-li zadat následující hodnoty, postupujte podle instrukcí pro zadávání dat na obrazovce. (Pořadí se může lišit v závislosti na mobilním zařízení nebo emulátoru, které používáte.)

    - **Náklad** – zadejte ID prvního nákladu, který jste vytvořili v předchozím postupu.
    - **Položka** – zadejte _A0001_, což je položka, která je pro toto náklad očekávána.
    - **Množství** – zadejte _3_. Povšimněte si, že toto množství je menší než očekávané množství. V tomto scénáři představte, že jste jako pracovník příjmu neměli čas pro evidenci všech množství pro tento náklad. Dále v tomto postupu zaznamenáte zbývající kusy opakováním tohoto kroku a nastavením pole **Množství** na _2_.

1. Pokračovat v procházení pracovního postupu, ponechat všechna ostatní pole prázdná nebo nastavit na výchozí hodnoty, dokud vám zařízení neinformuje o dokončení práce.
1. Ve webovém klientovi přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. V seznamu najděte náklad, který jste právě přijali, a výběrem hodnoty **ID nákladu** otevřete náklad. Všimněte si, že hodnota **Stav nákladu** zůstane _Expedováno_, ale hodnota **Množství vytvořené práce** na řádku nákladu se změnila na _3_.
1. V podokně akcí na kartě **Expedovat a přijmout** vyberte **Přijmout \> Příjemka produktu**. Vyberte **Ano** po zobrazení výzvy k potvrzení výběru.
1. V dialogovém okně **Zaúčtování příjemky produktu** zkontrolujte, ale neměňte zobrazené hodnoty, a pak vyberte **OK**.
1. Vrátíte se na stránku **Podrobností o nákladu** vybraného nákladu. Mějte na paměti následující body:

    - Pole **Stav nákladu** zůstává nastaveno na _Expedováno_.
    - V řádku nákladu zůstane hodnota **Množství** nákladu na _5_, což je původní množství pro náklad, a hodnota **Množství vytvořené práce** zůstává _3_.

1. Dokončete registraci zbývajícího množství do tohoto nákladu opakováním tohoto postupu. V kroku 3 však nastavte pole **Množství** na _2_.

Přijímající úkol pro první náklad je nyní dokončen. Byly vytvořeny dva deníky příjemek produktů, jedna pro každou z těchto dvou aktualizací příjemky produktu.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Zaregistrujte příjem množství, která byla doručena do druhého nákladu a na účet pro zvýšené množství

V tomto scénáři pracovník příjmu připíše množství, které je větší než množství, které existuje pro náklad. Navýšení příjmu bude povoleno, protože systém je nastaven tak, aby umožňoval navýšení dodávky.

1. Pomocí mobilního zařízení se přihlaste ke skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla _24_ ID uživatele a _1_ jako heslo.)
1. Vyberte položku nabídky _Přijetí položky nákladu_, kterou jste vytvořili pro tento scénář.
1. Chcete-li zadat následující hodnoty, postupujte podle instrukcí pro zadávání dat na obrazovce. (Pořadí se může lišit v závislosti na mobilním zařízení nebo emulátoru, které používáte.)

    - **Náklad** – zadejte druhé ID nákladu, které jste vytvořili dříve.
    - **Položka** – zadejte _A0001_, což je položka, která je pro toto náklad očekávána.
    - **Množství** – zadejte hodnotu _7_, což je zbývající množství, pro které má dodavatel oprávnění dodat jako součást celkového množství nákupní objednávky 12 (kde 10 je původní množství objednávky a 2 je povolené navýšení dodávky o 20 procent). Nezapomeňte, že 5 kusů již bylo v rámci prvního nákladu registrováno.

Druhý náklad byl nyní aktualizován o množství 7 a lze aktualizovat příjemku produktu na základě tohoto množství.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]