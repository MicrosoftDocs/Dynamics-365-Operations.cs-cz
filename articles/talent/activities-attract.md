---
title: Aktivity v procesech
description: Toto téma obsahuje informace o různých typech aktivit, které lze použít v procesu náboru.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c975b95e4195c795ec4c816b1f3a50461715feea
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/12/2019
ms.locfileid: "989907"
---
# <a name="activities-in-the-hiring-processes"></a>Aktivity v procesech náboru

[!include[banner](../includes/banner.md)]

Aktivity lze přidat jako součást procesu náboru v aplikaci Microsoft Dynamics 365 for Talent: Attract. Aktivity lze přidat do šablony procesu nebo přidávat přímo do procesu náboru v pracovní pozici. Při definování pracovní pozice je vybrána šablona procesu a u pracovní pozice jsou použity aktivity, které jsou součástí šablony. Pokud šablona není vybraná, použije se výchozí šablona. Proces náboru lze v pracovní pozici po použití šablony také změnit.

> [!NOTE] 
> Šablony procesu jsou k dispozici s doplňkem komplexního náboru. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aktivita potenciálního zákazníka

Aktivita potenciálního zákazníka určuje, zda lze do pracovní pozice přidávat potenciální zákazníky. Podle výchozího nastavení lze do pracovní pozice přidávat potenciální zákazníky. Pokud chcete aktivitu potenciálního zákazníka vypnout, nastavte možnost **Povolit potenciální zákazníky** na **Vypnuto**. Když je aktivita potenciálního zákazníka zapnutá, můžou manažeři náboru přidávat a zobrazovat potenciální zákazníky a v pracovní pozici se zobrazí karta **Potenciální zákazník**.

## <a name="application-activity"></a>Aktivita žádosti

Aktivita žádosti je povinná v šabloně procesu náboru. Pokud chcete odeslat e-mail uchazečům, když odešlou žádost nebo jsou přidáni do fáze žádosti, nastavte možnost **Odeslat e-mail uchazeči** na **Zapnuto**.

## <a name="interview-schedule-and-feedback-activity"></a>Plán pohovoru a aktivita zpětné vazby

Tato aktivita obsahuje tři složky: požadavek na dostupnost kandidáta, plán a zpětnou vazbu. Použijte aktivitu pohovoru v šabloně práce, pokud chcete zahrnout požadavek na dostupnost kandidáta, plán a zpětnou vazbu jako součást procesu, namísto jejich individuálního použití jako součástí náborového procesu. Další informace naleznete v tématu [Plánování pohovoru a zpětná vazba](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>Aktivity PowerApps

Aktivita PowerApps umožňuje vložit aplikaci Microsoft PowerApps do procesu náboru. Aplikace může být požadována pro všechny uchazeče, pouze interní uchazeče, pouze externí uchazečů nebo žádné uchazeče. Pokud je aplikace označena jako povinná, musí být dokončena předtím, než může fáze pokračovat. Aby byla práce považována za dokončenou, musí být v poli **JobApplicationStatus** zadána hodnota **Dokončeno**. Toto pole se nachází v entitě JobApplicationActivity, takže aplikace PowerApps bude muset aktualizovat toto pole, než bude možné pokračovat. Pokud aplikace není označena jako povinná, je aktivita volitelný krok a fáze můžete pokračovat, i když není aplikace dokončena.

Pokud chcete uložit aktivitu PowerApps do procesu náboru, je nutné zadat ID PowerApps. Pokud chcete vyhledat ID PowerApps, přejděte na [PowerApps](https://web.powerapps.com), vyberte **Aplikace** a pak vyberte **Detaily**.

Aktivita PowerApps je ve výchozím nastavení k dispozici pro náborového manažera, náborového pracovníka a jejich pověřené osoby. Vyberete-li možnost **Povolit přidání účastníků pro tuto aktivitu**, lze přidat další účastníky z náborového týmu pro aplikaci, která používá aktivitu PowerApps. Organizace má například vytvořenou aplikaci PowerApps, která je knihovnou otázek pohovoru pro technické funkce. Organizace nyní vypisuje výběrové řízení na nového vývojáře softwaru a přidala aktivitu PowerApps do procesu náboru na roli vývojáře softwaru. Pokud je vybraná možnost **Povolit přidávání účastníků pro tuto aktivitu**, náborář nebo manažer náboru, který zobrazuje uchazeče o roli vývojáře softwaru, může přidávat vedoucí pohovoru do aktivity PowerApps. Tyto osoby pak mohou zobrazit aplikaci, která obsahuje otázky pohovoru.

> [!NOTE]
> Aktivita PowerApps je dostupná pouze s doplňkem Komplexní nábor. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>Aktvita YouTube

Aktivita YouTube umožňuje sdílet video YouTube v rámci procesu náboru. Pokud chcete uložit aktivitu YouTube do procesu náboru, zadejte adresu URL videa YouTube. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivity PowerApps můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, video se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru.

> [!NOTE]
> Aktivita YouTube je dostupná pouze s doplňkem Komplexní nábor. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Aktivita Webový obsah

Aktivita Webový obsah umožňuje vložit online obsah do procesu náboru. Pokud chcete uložit aktivitu Webový obsah do procesu náboru, zadejte adresu URL obsahu. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivit PowerApps a YouTube můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, webový obsah se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru. Můžete vybrat velikost obsahu, který se zobrazí.

> [!NOTE]
> Aktivita Webový obsah je dostupná pouze s doplňkem Komplexní nábor. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Aktivita Microsoft Forms

Aktivita Microsoft Forms umožňuje vložit aktivitu Microsoft Forms do procesu náboru. Microsoft Forms vám umožňuje vytvářet kvízy, průzkumy a výzkumy veřejného mínění. Pokud chcete uložit aktivitu Microsoft Forms do procesu náboru, zadejte adresu URL formuláře. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivit PowerApps, YouTube a webového obsahu můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, formulář se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru.

V aplikaci Microsoft Forms mohou autoři měnit nastavení a umožnit tak uživatelům mimo jejich organizaci reagovat na průzkum nebo kvíz. V takovém případě uživatelé odesílají odpovědi anonymně. Pokud se chcete podívat, kdo vyplnil váš průzkum nebo kvíz, můžete vyžadovat, aby respondenti zadali jako součást průzkumu nebo kvízu své jméno.

> [!NOTE]
> Aktivita Microsoft Forms je dostupná pouze s doplňkem Komplexní nábor. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Aktivita nabídky

Šablona procesu náboru vyžaduje aktivitu Nabídka. Pokud chcete použít integrovanou aplikaci správy nabídky, nastavte možnost **Spustit aplikaci Správa nabídky při přípravě nabídky** na **Zapnuto**. Pokud je toto nastavení vypnuté, uchazeč se nezobrazí v aplikaci nabídka, takže budete muset ručně sledovat aktivitu nabídky uchazeče. Pokud chcete definovat, zda mohou manažeři náboru připravit nabídku pro uchazeče v aplikaci Nabídka, nastavte možnost **Manažeři náboru mohou připravit nabídku** na **Zapnuto**. Pokud má práce přidružených více pozic, můžete rozhodnout, zda připravíte více nabídek u stejného čísla pozice. Pokud chcete povolit pouze jednu nabídku pozice na pracovní pozici, nastavte **povolit pozice, které chcete opakovaně použít v rámci práce** na **vypnout**.

> [!NOTE]
> Integrovaná aplikace Offer Management je dostupná pouze s doplňkem Komplexní nábor. Další informace získáte v části [Funkce doplňku komplexního náboru aplikace Attract](./attract-comprehensive-hiring.md).


