---
title: Umístění zásob
description: Tento článek poskytuje informace o strategickém umístění zásob, což zahrnuje identifikaci bodů oddělení ve vašem dodavatelském řetězci, kde si můžete vytvořit zásoby na skladě a pomoci tak zkrátit dodací lhůty a absorbovat otřesy ve vašem dodavatelském řetězci.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186656"
---
# <a name="inventory-positioning"></a>Umístění zásob

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Strategické umístění zásob zahrnuje identifikaci bodů oddělení ve vašem dodavatelském řetězci, kde můžete vytvářet zásoby po ruce. Tento přístup se používá hlavně ke zkrácení dodacích lhůt a absorbování otřesů do vašeho dodavatelského řetězce. Umožňuje vám zmírnit „efekt biče“, protože variabilita poptávky neprochází celým dodavatelským řetězcem. (*Efekt biče* se týká toho, jak malé výkyvy poptávky na maloobchodní úrovni mohou způsobit progresivně větší výkyvy poptávky na úrovni velkoobchodu, distributora, výrobce a dodavatele surovin.)

Umístění zásob je prvním krokem plánování zdrojů materiálů řízených poptávkou (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Umístění zásob pro výrobu

Tato část poskytuje příklad, který ukazuje, jak se rozhodovat o umístění zásob, pokud vyrábíte typický polštářový produkt. Polštář má víceúrovňový kusovník, jak je znázorněno na následujícím obrázku.

![Příklad víceúrovňového kusovníku (BOM) pro polštářový produkt.](media/ddmrp-bom-example.png "Příklad víceúrovňového kusovníku (BOM) pro polštářový produkt")

### <a name="choose-your-decoupling-points"></a>Vyberte si body oddělení

Když vybíráte, kam umístit body oddělení, zvažte všechny následující aspekty každé položky v kusovníku jako kritéria:

- Externí variabilita
- Využití zásob a flexibilita zásob
- Ochrana kritického provozu
- Doba tolerance zákazníka
- Horizont viditelnosti prodejní objednávky
- Tržní potenciální dodací lhůta

V příkladu polštáře můžete svůj první oddělovací bod umístit na *pěnové předvalky* z následujících důvodů:

- Jsou materiály, které je obtížné získat a které se používají k výrobě pěnových bloků, a dostupnost je nestálá. Proto je splněno kritérium *vnější variabilita*.
- Pěnové předvalky lze řezat do mnoha různých tvarů a velikostí a vytvářet pěnové vložky pro další produkty, které vyrábíte, kromě polštáře. Proto je splněno kritérium *využití a flexibilita zásob*.

Potom byste mohli umístit svůj další bod oddělení na *textilní sada*, což je předstřižená polštářová látka. Možná si vyberete tento bod, protože máte pouze jeden stroj na řezání látek. Proto je splněno kritérium *ochrana kritického provozu*.

Nakonec můžete svůj poslední oddělovací bod umístit na hotový dobrý polštář. Můžete si vybrat tento bod, protože máte velmi nízkou *dobu tolerance zákazníka* na prodej, a protože váš *horizont viditelnosti prodejní objednávky* je poměrně krátký. Proto si chcete zajistit, že budete mít po ruce zásoby pro plnění příchozích objednávek. Můžete také nastavit vyšší cenu tím, že udržíte dodací lhůtu takto krátkou, což je to, na co odkazuje *doba realizace tržního potenciálu*.

Na základě této analýzy následující obrázek ukazuje, jak bude kusovník polštáře vypadat. Žluté symboly inventáře zvýrazňují body oddělení.

![Příklad kusovníku se zvýrazněnými body oddělení.](media/ddmrp-bom-decoupling-example.png "Příklad kusovníku se zvýrazněnými body oddělení")

### <a name="calculate-your-decoupled-lead-time"></a>Výpočet oddělené doby realizace

Tato část ukazuje, jak vypočítat nové doby realizace poté, co jste zavedli body oddělení.

Na následující ilustraci příkladu polštáře, který byl zahájen v předchozí části, jsou dodací lhůty zobrazeny v šedých polích v levém horním rohu každé součásti kusovníku. Pole s červeným obrysem označují položky, které řídí kumulativní dobu realizace (součet nejdelších dodacích lhůt na každé úrovni kusovníku). Tato doba realizace je 21 dní, když začínáte od nuly.

![Příklad kusovníku s dobou realizace.](media/ddmrp-bom-lead-times-example.png "Příklad kusovníku s dobou realizace")

Pokud však použijete body oddělení, které jste dříve zvolili, budou oddělené položky vždy skladem. Proto budou mít dobu realizace 0 (nula). Nová doba realizace pro polštář je nyní pouhých pět dní: dva dny na nákup nitě a tři dny na výrobu polštáře. Tato doba realizace se označuje jako *oddělená doba realizace*.

![Příklad oddělené doby realizace.](media/ddmrp-bom-decoupled-lead-time-example.png "Příklad oddělené doby realizace")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strategické umístění zásob v maloobchodním modelu

Protože maloobchodníci skladují pouze hotové výrobky, nejsou kusovníky problémem. Maloobchodníci však mohou stále používat DDMRP nastavením strategického umístění zásob a úrovní vyrovnávacích zásob na základě skladovacích míst v distribuční síti.

Následující obrázek ukazuje příklad společnosti, která má distribuční centrum v Seattlu a obchody v Bostonu, Atlantě a Portlandu.

![Oddělovací body na základě umístění v maloobchodním modelu.](media/ddmrp-retail-decoupl-points-example.png "Oddělovací body na základě umístění v maloobchodním modelu")

Můžete se rozhodnout, že doba přesunu produktu deky mezi distribučním centrem a prodejnami porušuje vaši *dobu tolerance zákazníka*, protože vaši zákazníci očekávají, že deka bude při jejich návštěvě skladem. V tomto případě zřídíte oddělovací bod pro deku v každém ze tří obchodů. Každý obchod bude mít různé úrovně vyrovnávacích zásob na základě dodacích lhůt, vzorců poptávky a tak dále.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Implementace umístění zásob v Dynamics 365 Supply Chain Management

Tato část popisuje, jak implementovat strategii umístění zásob v Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Nastavení skupin pokrytí položek, které vytvářejí body oddělení

Položky se stanou oddělovacími body, když patří do skupiny pokrytí, která je nakonfigurována pomocí hodnoty **Kód disponibility** *oddělovacího bodu*. Prvním krokem v procesu nastavení DDMRP je proto rozhodnutí, které skupiny disponibility musíte implementovat pro svou strategii DDMRP, a poté je vytvořit podle následujících kroků.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility**.
1. V podokně Akce vyberte možnost **Nová** a vytvořte novou skupinu disponibility.
1. Zadejte informace identifikující skupinu disponibility a pak vyberte kalendář, který se má použít.
1. Na kartě **Obecné** nastavte **Kód disponibility** na *Oddělovací bod*. Toto nastavení způsobí, že všechny položky, které patří do této skupiny pokrytí, budou považovány za oddělovací body pro DDMRP. Aktivuje také všechna nastavení DDMRP pro tuto skupinu, jak je popsáno dále v tomto postupu.
1. Na kartě **Ostatní** v části **Parametry DDMRP** nastavte následující pole:

    - **Koeficient doby realizace** – Zadejte koeficient (jako desetinnou hodnotu mezi 0 a 1), abyste řídili dopad, který by měla mít doba realizace při výpočtu minimální a maximální úrovně zásob pro položky v této skupině disponibility. Obecně platí, že čím delší je doba realizace položky, tím nižší by měl být její koeficient doby realizace. Nižší koeficient doby realizace vede k nižším minimálním a maximálním zásobám, a proto způsobuje menší a častější objednávky. Metodologie DDMRP doporučuje hodnotu mezi 0,20 a 0,40 pro položky, které mají dlouhou dobu realizace, mezi 0,41 a 0,60 pro položky, které mají střední dobu realizace, a mezi 0,61 a 1,00 pro položky, které mají krátkou dobu realizace. Další informace naleznete v tématu [Profil a úrovně vyrovnávacích zásob](ddmrp-buffer-profile-and-levels.md).
    - **Koeficient variability** – Zadejte koeficient (jako desetinnou hodnotu mezi 0 a 1), abyste řídili dopad, který by měla mít variabilita poptávky při výpočtu minimální a maximální úrovně zásob pro položky v této skupině disponibility. Obecně platí, že čím variabilnější je poptávka položky, tím vyšší by měl být její koeficient variability. Vyšší koeficient variability vede k vyšší minimální úrovni zásob. Metodologie DDMRP doporučuje hodnotu mezi 0,00 a 0,40 pro položky, které mají nízkou variabilitu, mezi 0,41 a 0,60 pro položky, které mají střední variabilitu, a mezi 0,61 a 1,00 pro položky, které mají vysokou variabilitu. Další informace naleznete v tématu [Profil a úrovně vyrovnávacích zásob](ddmrp-buffer-profile-and-levels.md).
    - **Minimální, maximální období a období pro objednání** – Určete, jak často se mají vypočítat hodnoty vyrovnávacích zásob (*Denně* nebo *Týdně*).

1. Na kartě **Ostatní** v části **Průměrná denní spotřeba** nastavte následující pole:

    - **Průměrná denní spotřeba na základě** – Vyberte, na kterých časových obdobích má být založen výpočet průměrné denní spotřeby (ADU). Vyberte jednu z následujících hodnot:

        - *Minulost* – Dívat se pouze na minulé použití za počet dní, které jsou uvedeny v poli **Minulé období (dny)**. ADU se vypočítá jako celková poptávka po položce během výpočtového období (v jednotkách zásob) dělená počtem dnů výpočtového období.
        - *Budoucnost* – Dívat se pouze na předpovídané budoucí použití (včetně předpovědí) za počet dní, které jsou uvedeny v poli **Budoucí období (dny)**. ADU se vypočítá jako celková poptávka po položce během výpočtového období (v jednotkách zásob) dělená počtem dnů výpočtového období. 
        - *Smíšené* – Dívat se na minulé i budoucí použití. Platní nastavení pro pole **Minulé období (dny)**, **pole Budoucí období (dny)** i smíšené možnosti. 

            *Smíšené ADU* = (\[*Minulé vážené* × *Minulé ADU*\] + \[*Budoucí vážení* × *Budoucí ADU*\]) ÷ (*Minulé vážené* + *Budoucí vážené*)

    - **Minulé období (dny)** – Zadejte počet minulých dnů (do dneška včetně), které by měl systém vzít v úvahu při výpočtu ADU položek v této skupině disponibility. Toto nastavení platí pouze tehdy, když je pole **Průměrná denní spotřeba na základě** nastaveno na *Minulost* nebo *Smíšené*.
    - **Budoucí období (dny)** – Zadejte počet budoucích dnů (do dneška až do zadaného dne), které by měl systém vzít v úvahu při výpočtu ADU položek v této skupině disponibility. Toto nastavení platí pouze tehdy, když je pole **Průměrná denní spotřeba na základě** nastaveno na *Budoucnost* nebo *Smíšené*.
    - **Relativní váha minulého období pro smíšenou průměrnou denní spotřebu** – Zadejte váhu (v procentech), která se má použít pro minulé období, kdy se počítá smíšená ADU. Toto nastavení platí pouze tehdy, když je pole **Průměrná denní spotřeba na základě** nastaveno na *Smíšené*.
    - **Relativní váha budoucího období pro smíšenou průměrnou denní spotřebu** – Zadejte váhu (v procentech), která se má použít pro budoucí období, kdy se počítá smíšená ADU. Toto nastavení platí pouze tehdy, když je pole **Průměrná denní spotřeba na základě** nastaveno na *Smíšené*.

1. Na všech ostatních kartách a polích zadejte podrobná nastavení, která se použijí pro výpočet požadavků na položky související se skupinou disponibility.

### <a name="set-an-item-as-a-decoupling-point"></a>Nastavení položky jako bodu oddělení

Chcete-li nastavit položku jako bod oddělení, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Najděte a vyberte uvolněnou položku, kterou chcete nastavit pro DDMRP.
1. V podokně akcí na kartě **Plánování** vyberte **Disponibilita položky**.
1. Na stránce **Disponibilita položky** může být již uvedeno několik záznamů disponibility položek, z nichž každý platí pro jinou kombinaci rozměrů skladu a produktu. Můžete vybrat existující záznam disponibility položky, který se vztahuje na dimenze, kde chcete vytvořit bod oddělení. Případně můžete vybrat **Nový** v podokně akcí a vytvořit nový záznam disponibility položky.
1. Nastavte záznam disponibility položky jako obvykle. Minimálně musíte zadat místo a sklad, kde bude bod oddělení platit.
1. Zatímco je stále vybrán příslušný záznam, vyberte kartu **Obecné** tab.
1. Zaškrtněte políčko **Použít konkrétní nastavení**.
1. Nastavte pole **Skupina disponibility** na skupinu disponibility, která je nastavena tak, aby vytvářela body oddělení (jak je popsáno v předchozí části).
1. Položka je nyní nakonfigurována jako oddělovací bod. Obvykle, když používáte DDMRP, zde také nakonfigurujete nastavení, která ovlivní velikost vyrovnávacích zásob a množství při objednání. Tuto konfiguraci však můžete provést později. Další informace o nastavení viz [Nastavení vyrovnávacích zásob pro položku bodu oddělení](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Chcete-li naplánovat položky, které nejsou oddělovacími body, postupujte podle stejných kroků jako při použití standardního plánování požadavků na materiál (MRP).
