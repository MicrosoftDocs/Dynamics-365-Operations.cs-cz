---
title: Vytvoření, schválení a podpis nabídek
description: Toto téma podrobně popisuje postup pro vytvoření, schválení a podepsání nabídky uchazeče pomocí aplikace Dynamics 365 for Talent.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303623"
---
# <a name="creating-approving-and-signing-offers"></a>Vytvoření, schválení a podpis nabídek

[!include[banner](../includes/banner.md)]

V mnoha případech musí být příprava balíčku s nabídkou pro uchazeče velmi rychlý proces.
Použití šablon nastavených správcem systému Attract zkrátí dobu a úsilí, kterou tvůrci nabídky stráví přípravou a zasláním nabídek uchazeči.

## <a name="create-an-offer"></a>Vytvoření nabídky

Když je zapnutá aplikace Správa nabídky, může libovolný uživatel s rolí manažera náboru nebo náboráře připravit balíček nabídky pro zájemce. Při přípravě nabídky postupujte takto.

1.  Přejděte na pracovní pozici a žádost uchazeče, pro které nabídku vytváříte.

1.  Přejděte na **Fáze nabídky** a klikněte na **Připravit nabídku**.

    Budete přesměrováni do aplikace Nabídka, kde uvidíte uchazeče se stavem **nový**. Zobrazí se také jiné nabídky, ke kterým přispíváte jako tvůrce nebo schvalovatel.

1.  Klikněte na **Připravit nabídku**. 
    
    Zobrazí se výběr jiných balíčků nabídky, které jsou k dispozici od správce.

1.  Vyberte balíček a klikněte na tlačítko **Hotovo** pro zahájení přípravy nabídky.

    Načte se šablona balíčku nabídky s odpovídající pracovní pozicí a podrobnostmi o uchazeči, které jsou v nabídce zadány.

1.  Všechny zástupné symboly dat nabídky, které jsou součástí balíčku nabídky, jsou zobrazeny na úvodní stránce. Všechny hodnoty lze zadat do balíčku na této stránce.

    Na úvodní stránce se také zobrazí všechny šablony dokumentu nabídky, které jsou součástí balíčku nabídky.

1.  Nyní lze upravovat obsah nabídky, v závislosti na způsobu konfigurace šablony správcem.

1.  Pokud potřebujete odebrat dokumenty označené jako nevyžádané, můžete to provést.

1. Po naplnění všech zástupných symbolů nabídky klikněte na tlačítko **Uložit**, aby se uložil koncept nabídky.

>[!NOTE]
> Po uložení návrhu můžete odstranit verzi konceptu nabídky nebo vybrat novou šablonu balíčku, pokud to je potřeba.


## <a name="approve-an-offer"></a>Schválení nabídky

Většina nabídek musí projít schvalovacím procesem pro zajištění, že nabídka splňuje nezbytné standardy. Pokud nabídka neodpovídá standardům, například, pokud tvůrce nabídky nepostupoval podle pravidel dat nabídky a přepsal hodnoty nabídky, bude schvalovací proces nařízen. Pokud chcete odeslat nabídku ke schválení, postupujte takto.

1.  Když je nabídka ve stavu konceptu, přidejte schvalovatele na **panel Schvalovatel**. 
    >[!NOTE]
    > Při výchozím nastavení jsou jako schvalovatelé přidání manažeři náboru. Jako schvalujícího nabídky můžete vybrat libovolného uživatele ve vaší organizaci.

1.  V případě potřeby přiřazujte schvalující metodou postupného schvalování nebo paralelního schvalování. Tato možnost bude k dispozici pouze v případě, že tak byla nakonfigurována správcem.
    >[!NOTE]
    > Pokud je proces schvalování sekvenční, můžete upravit pořadí schvalovatelů v případě potřeby.

1.  Po dokončení definování řetězce schvalování lze dále upravit obsah e-mailu o schválení a následně odeslat oznámení schvalovatelům. Klikněte na **Odeslat schvalovatelům**.
    >[!NOTE]
    > Pokud byla nabídka nestandardní, je nutné zadat odůvodnění.

1.  Pokud tvůrce nabídky zvolí možnost přeskočení schvalovatele, může zadat poznámku a přejít k dalšímu schvalovateli.

Schvalující obdrží e-mail s žádostí o schválení nabídky. Mohou kliknutím na odkaz v e-mailu otevřít nabídku, přečíst si celý balíček nabídky a buď ji schválit nebo odeslat zpět jejímu autorovi. Schvalovatelé nabídky budou muset přidat další poznámku, pokud odmítají balíček nabídky, pro další úpravy. 

V případech, kdy byla vytvořena nová verze nabídky předtím, než schvalovatel jednal, nebude schvalovatel moci schválit nebo zamítnout nabídku.

## <a name="offer-versioning"></a>Vytváření verzí nabídky 

Když byla nabídka přijata nebo odeslána zpět pro další úpravy, můžete vybrat možnost **povolit úpravy**, chcete-li vytvořit novou verzi nabídky. Nová verze nabídky obsahuje všechny hodnoty data nabídky a seznam schvalovatelů přenesené z poslední verze. 

Schvalující může přepínat mezi různými verzemi nabídky, pokud s nimi byly verze sdíleny ke schválení. Schvalovatel nebo tvůrce nabídky také může odstranit specifickou verzi konceptu nabídky, aby bylo možné přejít na předchozí stav.


## <a name="send-an-offer-to-a-candidate"></a>Odeslání nabídky uchazeči 

Po uložení, schválení a připravenosti odeslat nabídku uchazeči klikněte na **Odeslat uchazeči**.

Existuje několik akcí, které lze provést před odesláním nabídky uchazeči.
-  Můžete zobrazit seznam dokumentů, které jsou součástí balíčku nabídky, který bude odeslán uchazeči.

-  Můžete zadat datum vypršení platnosti nabídky. Očekává se, že uchazeči přijmou nebo odmítnou nabídku před datem vypršením platnosti.  Uchazeči bude zasláno připomenutí 48 hodin před vypršením platnosti nabídky.

-  Mohou existovat další dokumenty, které mají být zahrnuty do procesu přijetí nabídky. Budete mít možnost uvést požadovaný typ dokumentu.

- Možnost elektronického podpisu Pokud byla jako preferovaná metoda elektronického podpisu vybrána Adobe Sign, musí si autoři nabídky přidat licenci Adobe Sign. To lze provést dvěma způsoby. Přejděte na uživatelské **nastavení** v části **nabídka** pod **připojení** připojit **Adobe Sign**. Případně se zobrazí výzva k připojení nabídky odeslání na obrazovku uchazeče, pokud nebylo připojení navázáno na základě uživatelského nastavení. 

> [!NOTE]
> Stačí, když uživatelé připojí účty Adobe Sign jednou. Stejná uživatelská licence se použije pro všechny budoucí nabídky balíčků, které bude odesílat stejný uživatel. 

-  Podle potřeby můžete zobrazit a upravit šablonu e-mailů.

Když je nabídka připravena a kliknete na tlačítko **Odeslat uchazeči**, uchazeč obdrží e-mail, že nabídka čeká na kontrolu.


## <a name="candidates-actions-after-receiving-an-offer"></a>Akce uchazeče po přijetí nabídky

Poté, co byl uchazeč upozorněn, že s ním byla sdílena nabídka, může kliknout na odkaz v e-mailu pro přechod do řídicího panelu aplikaci a zobrazení nabídky. Řídicí panel zobrazí uchazeči všechny aktivity, které je ještě nutné provést.

1.  Pokud chce uchazeč zobrazit nabídku a všechny související dokumenty, musí kliknout na **Zobrazit nabídku**.

    Uchazeči také mohou stáhnout balíček nabídky ve formátu .zip.

1.  Pokud chce uchazeč nabídku přijmout, musí kliknout na **Přejít na podpis** u každého dokumentu, který je součástí balíčku nabídky.

1.  Poté, co byly všechny dokumenty jednotlivě podepsány a přijaty, musí uchazeč vybrat dokončení procesu přijetí kliknutím na **Přijmout nabídku** v horní části stránky.

1.  Pokud chce uchazeč nabídku odmítnout, musí kliknout na **Odmítnout nabídku** v horní části stránky, vybrat odpovídající důvod, podle potřeby přidat poznámku a kliknout na tlačítko **odmítnout**.

1.  Po přijetí nebo odmítnutí nabídky může uchazeč dále zůstat v zobrazení nabídky nebo se vrátit zpět do řídicího panelu aplikace.

1.  Pokud byly v rámci procesu přijetí nabídky požadovány jiné dokumenty, uchazeč by měl zvolit odesílání dokumentů podle potřeby a označit je v požadovaném typu dokumentu.

1.  Autor nabídky bude upozorněn, jakmile budou všechny dokumenty odeslány a podepsán balíček nabídky.


## <a name="withdrawing-an-offer"></a>Stažení nabídky

Nabídku lze uchazeči kdykoli odmítnout z různých důvodů. 
1.  Kliknutím na tlačítko se třemi tečkami (**...**) proveďte odmítnutí nabídky a klikněte na tlačítko **Odmítnout nabídku**. 

2. Zobrazí se zpráva s dotazem zda byl uchazeč kontaktován ohledně změny stavu. Jestliže uchazeč nebyl dosud kontaktován, budete mít možnost odeslat mu e-mail s informací o dalších akcích. 

   Nabídka již nebude uchazeči přístupná.


## <a name="closing-an-offer"></a>Uzavření nabídky 

Po přijetí, odmítnutí nebo odebrání nabídky nebudou potřeba žádné další akce. Nabídku můžete zavřít, aby nebylo možné provádět žádné další úpravy tohoto balíčku nabídky.
