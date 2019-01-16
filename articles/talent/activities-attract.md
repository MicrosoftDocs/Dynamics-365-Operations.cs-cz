---
title: Aktivity v procesech
description: "Toto téma obsahuje informace o různých typech aktivit, které lze použít v procesu náboru."
author: 
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 4f59193991420fd9ec05a83049e569058bf81932
ms.contentlocale: cs-cz
ms.lasthandoff: 12/07/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aktivity v procesech náboru

[!include[banner](../includes/banner.md)]

Aktivity lze přidat jako součást procesu náboru v aplikaci Microsoft Dynamics 365 for Talent: Attract. Aktivity lze přidat do šablony procesu nebo přidávat přímo do procesu náboru v pracovní pozici. Při definování pracovní pozice je vybrána šablona procesu a u pracovní pozice jsou použity aktivity, které jsou součástí šablony. Pokud šablona není vybraná, použije se výchozí šablona. Proces náboru lze v pracovní pozici po použití šablony také změnit.

> [!NOTE] 
> Šablony procesu jsou k dispozici s doplňkem komplexního náboru.

## <a name="prospect-activity"></a>Aktivita potenciálního zákazníka

Aktivita potenciálního zákazníka určuje, zda lze do pracovní pozice přidávat potenciální zákazníky. Podle výchozího nastavení lze do pracovní pozice přidávat potenciální zákazníky. Pokud chcete aktivitu potenciálního zákazníka vypnout, nastavte možnost **Povolit potenciální zákazníky** na **Vypnuto**. Když je aktivita potenciálního zákazníka zapnutá, můžou manažeři náboru přidávat a zobrazovat potenciální zákazníky a v pracovní pozici se zobrazí karta **Potenciální zákazník**.

## <a name="application-activity"></a>Aktivita žádosti

Aktivita žádosti je povinná v šabloně procesu náboru. Pokud chcete odeslat e-mail uchazečům, když odešlou žádost nebo jsou přidáni do fáze žádosti, nastavte možnost **Odeslat e-mail uchazeči** na **Zapnuto**.

## <a name="scheduler-activity"></a>Aktivita plánovače

Aktivita plánovače je volitelná. Tato aktivita obsahuje dvě složky: dostupnost kandidáta a plán. Dostupnost komponenty Uchazeč umožňuje používat e-mail k vyžádání dostupnosti uchazeče. Komponenta Plán umožňuje plánování pohovorů s uchazečem a týmem náboru. V aktivitě Plánovač lze konfigurovat následující možnosti: **Požadovat dostupnost uchazeče**, **Online schůzka** a **Odeslání e-mailu uchazeči**.

- Pokud chcete odeslat uchazečům e-mail s dotazem na dostupnost, nastavte možnost **Požadovat dostupnost uchazeče** na **Zapnuto**. Pokud nastavíte tuto možnost na **Vypnuto**, tento krok se v procesu náboru na pracovní pozici nezobrazí.
- Pokud chcete živě streamovat nebo uskutečnit živý konferenční hovor pomocí Skypu pro firmy, nastavte hodnotu v poli **Online schůzka** na **Skype pro firmy**. Do žádosti o schůzku s pohovorem, která je rozeslána vedoucím pohovorů, pak bude přidán správný odkaz **Připojit ke skypové schůzce**.
- Pokud chcete odeslat uchazečům e-mail pro dokončení plánu, nastavte možnost **Odeslat uchazeči e-mail** na **Zapnuto**. Pokud tuto možnost nastavíte na **Vypnuto**, uchazeči obdrží plán pohovoru pouze v případě, že se přihlásí na portál pro uchazeče.

## <a name="feedback-activity"></a>Aktivita zpětné vazby

Aktivita zpětné vazby je volitelná. Tato aktivita umožňuje účastníkům pohovoru zadat doporučení pro uchazeče. Mohou rovněž zadat jakékoli komentáře ke zpětné vazbě. Pokud zapnete možnost **Zdědit účastníky zpětné od náborového týmu**, budou do aktivity zpětné vazby automaticky zadáni náborář, manažer náboru a vedoucí pohovoru. Organizace mohou tazatelům povolit zobrazení zpětné vazby ostatních předtím, než odešlou vlastní zpětnou vazbu. Organizace může také povolit tazatelům úpravu zpětné vazby po odeslání.

## <a name="interview-activity"></a>Aktivita pohovoru

Aktivita pohovoru je volitelná. Tato aktivita obsahuje tři složky: dostupnost kandidáta, plán a zpětná vazba. Dostupnost komponenty Uchazeč umožňuje používat e-mail k vyžádání dostupnosti uchazeče. Komponenta Plán umožňuje plánování pohovorů s uchazečem a týmem náboru. V aktivitě Plánovač lze konfigurovat následující možnosti: **Požadovat dostupnost uchazeče**, **Online schůzka** a **Odeslání e-mailu uchazeči**.

- Pokud chcete odeslat uchazečům e-mail s dotazem na dostupnost, nastavte možnost **Požadovat dostupnost uchazeče** na **Zapnuto**. Pokud nastavíte tuto možnost na **Vypnuto**, tento krok se v procesu náboru na pracovní pozici nezobrazí.
- Pokud chcete živě streamovat nebo uskutečnit živý konferenční hovor pomocí Skypu pro firmy, nastavte hodnotu v poli **Online schůzka** na **Skype pro firmy**. Do žádosti o schůzku s pohovorem bude přidán správný odkaz **Připojit ke skypové schůzce**.
- Pokud chcete odeslat uchazečům e-mail pro dokončení plánu, nastavte možnost **Odeslat uchazeči e-mail** na **Zapnuto**. Pokud tuto možnost nastavíte na **Vypnuto**, uchazeči obdrží plán pohovoru pouze v případě, že se přihlásí na portál pro uchazeče.

>[!NOTE]
> - Pro všechny pohovory 1:1 jsou připomenutí odesílána tazatelům každých 24 hodin, pokud nereagoval (přejetí nebo zamítnutí) na žádost o pohovor.
> - Pro všechny panelové pohovory nejsou žádná automatizovaná připomenutí na reagování na žádost o pohovor. Pokud chcete připomenutí spustit ručně, upravte pohovor a použijte možnost **aktualizovat a odeslat** k odeslání žádosti zpět tazatelům.

Součást Zpětná vazba komponenty umožňuje zadávat doporučení pro uchazeče. Mohou rovněž zadat jakékoli komentáře ke zpětné vazbě. Pokud zapnete možnost **Zdědit účastníky zpětné od náborového týmu**, budou do složky zpětné vazby automaticky zadáni náborář, manažer náboru a vedoucí pohovoru. Organizace mohou tazatelům povolit zobrazení zpětné vazby ostatních předtím, než odešlou vlastní zpětnou vazbu. Organizace může také povolit tazatelům úpravu zpětné vazby po odeslání.

## <a name="powerapps-activity"></a>Aktivita PowerApps

Aktivita PowerApps umožňuje vložit aplikaci Microsoft PowerApps do procesu náboru. Aplikace může být požadována pro všechny uchazeče, pouze interní uchazeče, pouze externí uchazečů nebo žádné uchazeče. Pokud je aplikace označena jako povinná, musí být dokončena předtím, než může fáze pokračovat. Pokud aplikace není označena jako povinná, je aktivita volitelný krok a fáze můžete pokračovat, i když není aplikace dokončena.

Pokud chcete uložit aktivitu PowerApps do procesu náboru, je nutné zadat ID PowerApps. Pokud chcete vyhledat ID PowerApps, přejděte na [PowerApps](https://web.powerapps.com), vyberte **Aplikace** a pak vyberte **Detaily**.

Vyberete-li možnost **Povolit přidání účastníků pro tuto aktivitu**, lze přidat další přispěvatele pro aplikace, která používá aktivitu PowerApps. Organizace má například vytvořenou aplikaci PowerApps, která je knihovnou otázek pohovoru pro technické funkce. Organizace nyní vypisuje výběrové řízení na nového vývojáře softwaru a přidala aktivitu PowerApps do procesu náboru na roli vývojáře softwaru. Pokud je vybraná možnost **Povolit přidávání účastníků pro tuto aktivitu**, náborář nebo manažer náboru, který zobrazuje uchazeče o roli vývojáře softwaru, může přidávat osoby do aktivity PowerApps. Tyto osoby pak mohou zobrazit aplikaci, která obsahuje otázky pohovoru.

> [!NOTE]
> Aktivita PowerApps je dostupná pouze s doplňkem Komplexní nábor.

## <a name="youtube-activity"></a>Aktivita YouTube

Aktivita YouTube umožňuje sdílet v rámci procesu náboru video YouTube. Pokud chcete uložit aktivitu YouTube do procesu náboru, zadejte adresu URL videa YouTube. Pokud jde o aktivitu PowerApps, můžete povolit účastníkům, aby se přidali do aktivity. Vyberete-li možnost **Zobrazit pouze uchazeči**, video se zobrazí pouze jako součást zkušenosti uchazeče. Nezobrazuje se v procesu náboru v systému Attract.

> [!NOTE]
> Aktivita YouTube je dostupná pouze s doplňkem Komplexní nábor.

## <a name="web-content-activity"></a>Aktivita Webový obsah

Aktivita Webový obsah umožňuje vložit online obsah do procesu náboru. Pokud chcete uložit aktivitu Webový obsah do procesu náboru, zadejte adresu URL obsahu. Pokud jde o aktivity PowerApps a YouTube, můžete povolit účastníkům, aby se přidali do aktivity. Vyberete-li možnost **Zobrazit pouze uchazeči**, obsah se zobrazí pouze jako součást zkušenosti uchazeče. Nezobrazuje se v procesu náboru v systému Attract. Můžete vybrat velikost obsahu, který se zobrazí.

> [!NOTE]
> Aktivita Webový obsah je dostupná pouze s doplňkem Komplexní nábor.

## <a name="microsoft-forms-activity"></a>Aktivita Microsoft Forms

Aktivita Microsoft Forms umožňuje vložit aplikaci Microsoft Microsoft Forms do procesu náboru. Microsoft Forms vám umožňuje vytvářet kvízy, průzkumy a výzkumy veřejného mínění. Pokud chcete uložit aktivitu Microsoft Forms do procesu náboru, zadejte adresu URL formuláře. Pokud jde o aktivity PowerApps, YouTube a Webový obsah, můžete povolit účastníkům, aby se přidali do aktivity. Vyberete-li možnost **Zobrazit pouze uchazeči**, formulář se zobrazí pouze jako součást zkušenosti uchazeče. Nezobrazuje se v procesu náboru v systému Attract.

V aplikaci Microsoft Forms mohou autoři měnit nastavení a umožnit tak uživatelům mimo jejich organizaci reagovat na průzkum nebo kvíz. V takovém případě uživatelé odesílají odpovědi anonymně. Pokud se chcete podívat, kdo vyplnil váš průzkum nebo kvíz, můžete vyžadovat, aby respondenti zadali jako součást průzkumu nebo kvízu své jméno.

> [!NOTE]
> Aktivita Microsoft Forms je dostupná pouze s doplňkem Komplexní nábor.

