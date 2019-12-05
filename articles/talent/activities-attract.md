---
title: Přidání aktivit do procesu náboru
description: Toto téma obsahuje informace o různých typech aktivit, které lze přidat do procesu náboru v aplikaci Microsoft Dynamics 365 Talent – Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
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
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833270"
---
# <a name="add-activities-to-a-hiring-process"></a>Přidání aktivit do procesu náboru

[!include [banner](includes/banner.md)]

Aktivity lze přidat jako součást procesu náboru v aplikaci Microsoft Dynamics 365 Talent: Attract. Aktivity lze přidat do šablony procesu nebo přidávat přímo do procesu náboru v pracovní pozici. Při definování pracovní pozice je vybrána šablona procesu a u pracovní pozice jsou použity aktivity, které jsou součástí šablony. Pokud šablona není vybraná, použije se výchozí šablona. Proces náboru lze v pracovní pozici po použití šablony také změnit.

> [!NOTE] 
> Šablony procesu jsou k dispozici s doplňkem komplexního náboru. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aktivita potenciálního zákazníka

Aktivita potenciálního zákazníka určuje, zda lze do pracovní pozice přidávat potenciální zákazníky. Podle výchozího nastavení lze do pracovní pozice přidávat potenciální zákazníky. Pokud chcete aktivitu potenciálního zákazníka vypnout, nastavte možnost **Povolit potenciální zákazníky** na **Vypnuto**. Když je aktivita potenciálního zákazníka zapnutá, můžou manažeři náboru přidávat a zobrazovat potenciální zákazníky a v pracovní pozici se zobrazí karta **Potenciální zákazník**.

> [!NOTE]
> Chcete-li povolit přidávání kandidátů do úlohy ze služby LinkedIn, je nutné nastavit možnost **Povolit potenciální zákazníky** na **On**.

## <a name="application-activity"></a>Aktivita žádosti

Aktivita žádosti je povinná v šabloně procesu náboru. Pokud chcete odeslat e-mail uchazečům, když odešlou žádost nebo jsou přidáni do fáze žádosti, nastavte možnost **Odeslat e-mail uchazeči** na **Zapnuto**.

## <a name="interview-schedule-and-feedback-activity"></a>Plán pohovoru a aktivita zpětné vazby

Tato aktivita obsahuje tři složky: požadavek na dostupnost kandidáta, plán a zpětnou vazbu. Použijte aktivitu pohovoru v šabloně práce, pokud chcete zahrnout požadavek na dostupnost kandidáta, plán a zpětnou vazbu jako součást procesu, namísto jejich individuálního použití jako součástí náborového procesu. Další informace naleznete v tématu [Plánování pohovoru a zpětná vazba](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Aktvita Power Apps

Aktivita Power Apps umožňuje vložit aplikaci Microsoft Power Apps do procesu náboru. Aplikace může být požadována pro všechny uchazeče, pouze interní uchazeče, pouze externí uchazečů nebo žádné uchazeče. Pokud je aplikace označena jako povinná, musí být dokončena předtím, než může fáze pokračovat. Aby byla práce považována za dokončenou, musí být v poli **JobApplicationStatus** zadána hodnota **Dokončeno**. Toto pole se nachází v entitě JobApplicationActivity, takže aplikace Power Apps bude muset aktualizovat toto pole, než bude možné pokračovat. Pokud aplikace není označena jako povinná, je aktivita volitelný krok a fáze můžete pokračovat, i když není aplikace dokončena.

Pokud chcete uložit aktivitu Power Apps do procesu náboru, je nutné zadat ID Power Apps. Pokud chcete vyhledat ID Power Apps, přejděte na [Power Apps](https://web.powerapps.com) , vyberte **Aplikace** a pak vyberte **Detaily**.

Aktivita Power Apps je ve výchozím nastavení k dispozici pro náborového manažera, náborového pracovníka a jejich pověřené osoby. Vyberete-li možnost **Povolit přidání účastníků pro tuto aktivitu**, lze přidat další účastníky z náborového týmu pro aplikaci, která používá aktivitu Power Apps. Organizace má například vytvořenou aplikaci Power Apps, která je knihovnou otázek pohovoru pro technické funkce. Organizace nyní vypisuje výběrové řízení na nového vývojáře softwaru a přidala aktivitu Power Apps do procesu náboru na roli vývojáře softwaru. Pokud je vybraná možnost **Povolit přidávání účastníků pro tuto aktivitu**, náborář nebo manažer náboru, který zobrazuje uchazeče o roli vývojáře softwaru, může přidávat vedoucí pohovoru do aktivity Power Apps. Tyto osoby pak mohou zobrazit aplikaci, která obsahuje otázky pohovoru.

> [!NOTE]
> Aktivita Power Apps je dostupná pouze s doplňkem Komplexní nábor. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>Aktvita YouTube

Aktivita YouTube umožňuje sdílet video YouTube v rámci procesu náboru. Pokud chcete uložit aktivitu YouTube do procesu náboru, zadejte adresu URL videa YouTube. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivity Power Apps můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, video se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru.

> [!NOTE]
> Aktivita YouTube je dostupná pouze s doplňkem Komplexní nábor. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Aktivita Webový obsah

Aktivita Webový obsah umožňuje vložit online obsah do procesu náboru. Pokud chcete uložit aktivitu Webový obsah do procesu náboru, zadejte adresu URL obsahu. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivit Power Apps a YouTube můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, webový obsah se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru. Můžete vybrat velikost obsahu, který se zobrazí.

> [!NOTE]
> Aktivita Webový obsah je dostupná pouze s doplňkem Komplexní nábor. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Aktivita Microsoft Forms

Aktivita Microsoft Forms umožňuje vložit aktivitu Microsoft Forms do procesu náboru. Microsoft Forms vám umožňuje vytvářet kvízy, průzkumy a výzkumy veřejného mínění. Pokud chcete uložit aktivitu Microsoft Forms do procesu náboru, zadejte adresu URL formuláře. Můžete se rozhodnout zobrazit obsah pro **náborový tým**, **pouze interní uchazeče**, **pouze externí uchazeče** nebo **všechny uchazeče**. Stejně jako u aktivit Power Apps, YouTube a webového obsahu můžete povolit účastníkům náborového týmu, aby se přidali do aktivity. Rozhodnete-li se zobrazit obsah pro uchazeče, formulář se zobrazí pouze v rámci zkušeností uchazeče a nikoli v rámci procesu náboru.

V aplikaci Microsoft Forms mohou autoři měnit nastavení a umožnit tak uživatelům mimo jejich organizaci reagovat na průzkum nebo kvíz. V takovém případě uživatelé odesílají odpovědi anonymně. Pokud se chcete podívat, kdo vyplnil váš průzkum nebo kvíz, můžete vyžadovat, aby respondenti zadali jako součást průzkumu nebo kvízu své jméno.

> [!NOTE]
> Aktivita Microsoft Forms je dostupná pouze s doplňkem Komplexní nábor. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Aktivita nabídky

Šablona procesu náboru vyžaduje aktivitu Nabídka. Pokud chcete použít integrovanou aplikaci správy nabídky, nastavte možnost **Spustit aplikaci Správa nabídky při přípravě nabídky** na **Zapnuto**. Pokud je toto nastavení vypnuté, uchazeč se nezobrazí v aplikaci nabídka, takže budete muset ručně sledovat aktivitu nabídky uchazeče. Pokud chcete definovat, zda mohou manažeři náboru připravit nabídku pro uchazeče v aplikaci Nabídka, nastavte možnost **Manažeři náboru mohou připravit nabídku** na **Zapnuto**. Pokud má práce přidružených více pozic, můžete rozhodnout, zda připravíte více nabídek u stejného čísla pozice. Pokud chcete povolit pouze jednu nabídku pozice na pracovní pozici, nastavte **povolit pozice, které chcete opakovaně použít v rámci práce** na **vypnout**.

> [!NOTE]
> Integrovaná aplikace Offer Management je dostupná pouze s doplňkem Komplexní nábor. Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).


