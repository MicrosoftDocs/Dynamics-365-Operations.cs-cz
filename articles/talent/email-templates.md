---
title: Šablony e-mailů
description: Toto téma obsahuje informace o šablonách e-mailu, které lze vytvořit a používat v aplikaci Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1c7c017cce26b6b250d899bba891d6823b40c282
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729719"
---
# <a name="email-templates"></a>Šablony e-mailů
[!include[banner](../includes/banner.md)]

Pomocí knihovny šablon e-mailu mohou správci vytvářet jednotný motiv a značky všech e-mailů zasílaných z aplikace Microsoft Dynamics 365 for Talent: Attract and Offer. Správci také mohou také uspořádat sadu šablon obsahu e-mailů, kterou mohou využívat ostatní uživatelé. Náborový tým může tyto šablony používat ve svém workflowu k efektivnějšímu odesílání e-mailů. Některé e-mailové zprávy jsou nakonfigurovány na automatické odeslání a správce může použít knihovnu šablon e-mailu pro přizpůsobení obsahu těchto e-mailů.

> [!NOTE]
> Aby bylo možné E-mailové šablony používat, musí mít organizace doplněk Komplexní nábor.

## <a name="global-template-configurations"></a>Konfigurace globální šablony

Aby bylo možné vytvořit konzistentní značkování veškeré e-mailové komunikace, musí správce nejprve nastavit globální záhlaví a zápatí pro všechny e-mailové šablony. V centru pro správu na kartě **Nastavení e-mailové šablony** v části **záhlaví** může správce nahrát obrázek, který bude použit jako záhlaví nebo banner u všech e-mailů. Obrázek může být logo společnosti, hlavička a nebo jiný reprezentativní obrázek. Doporučujeme šířku mezi 25 a 800 pixely a výšku mezi 25 a 150 pixely vzhledem k tomu, že tyto rozměry jsou optimální pro většinu e-mailových klientů, jako je například aplikace Microsoft Outlook. Obrázek musí být ve formátu JPEG, JPG, PNG nebo SVG a velikost souboru musí být menší než 1 MB (megabajt). Po nahrání obrázku se generuje a zobrazí náhled záhlaví. Pokud záhlaví obrázku musí odebráno a nahrazeno, může správce použít možnost **Odebrat** nad náhledem.

V části **zápatí** může správce poskytnout odkazy na zásady ochrany osobních údajů společnosti pro komunikaci a podmínky. Tyto odkazy jsou zahrnuty do zápatí, které je automaticky generováno. Následně se zobrazí náhled tohoto zápatí. Správce může také zvolit konkrétní jazyk, ve kterém budou e-mailová zápatí odeslána jako součást všech e-mailů. Pro shromáždění souhrnné tabulky s pohovorem bude také použita stejná konfigurace jazyka. 

Je nutné před zavřením centra pro správu uložit změny.

> [!NOTE] 
> Záhlaví a zápatí jsou globální nastavení pro všechny e-maily. Proto se objevují ve všech e-mailech odeslaných prostřednictvím aplikace Attract. Pokud nastavení není nakonfigurováno, záhlaví a zápatí bude vynecháno ve všech e-mailech.

## <a name="email-template-library"></a>Knihovna šablon e-mailu 

Po nastavení konfigurace globální šablony může správce začít vytvářet a pořádat šablony pro všechny e-mailové zprávy odeslané z aplikace Attract a Offer. Knihovna šablon e-mailu je k dispozici pouze pro správce. Pokud chcete otevřít knihovnu, v hlavní navigačního nabídce vyberte kartu **E-mailové šablony**. Knihovna je kategorizována podle různých aktivit v aplikaci Attract, pro které musí být odeslány e-maily, jako je například plánování, hodnocení a vytvoření pracovního místa a nabídky. Správce může vybrat libovolnou kategorii k zobrazení všech typů e-mailů spojených s aktivitou. Vyberte například **plánování**, pokud chcete zobrazit různé typy e-mailových zpráv odeslaných během procesu plánování a všechny šablony, které jsou k dispozici pro každý typ e-mailu. Každý pododdíl kategorie představuje typ e-mailu.

Některé typy e-mailů mohou mít více příjemců. Například v kategorii **Plánování** jsou e-maily odeslané v případě, kdy je potřeba souhrn plánu pohovoru, uchazečům i vedoucím pohovorů. Každý oddíl má dva hlavní sloupce: **Název šablony** a **Příjemce**. Každý řádek v oddílu představuje jednu šablonu pro typ e-mailu. Nejprve se zobrazí symbol zámku na řádku pro každou šablonu. Tento symbol označuje, že šablona je standardní šablona, která je součástí aplikace Attract a nelze ji odstranit. Správce může pro všechny šablony použít tlačítko se třemi tečkami (**...**) k duplikování šablony, jejímu nastavení jako výchozí nebo odstranění. Pokud je šablona nastavená jako výchozí, může nastat jeden ze dvou typů chování. Chování je označeno odznakem nebo odznaky, které se zobrazí v řádku šablony:

- **Výchozí** – Tento odznak označuje, že šablona je výchozí pro e-mail, který je odeslán a že tyto informace budou zadány do šablony, když uživatel odešle e-mail tohoto konkrétního typu.
- **Výchozí** + **Automaticky odeslané** – tato kombinace odznaků označuje, že je šablona aktivní pro systémem generované e-maily, které se odesílají automaticky.

Pokud chcete upravit šablonu, vyberte řádek a proveďte změny šablony.

> [!NOTE]
> Každý příjemce konkrétního typu e-mailu má výchozí šablonu. Všechny standardní šablony aplikace Attract jsou nastaveny jako výchozí šablony, dokud správce nevytvoří novou šablonu pro konkrétní typ e-mailu a nenastaví ho jako výchozí šablonu.

## <a name="create-a-template"></a>Vytvořit šablonu

Chcete-li vytvořit šablonu, v pravém horním rohu knihovny šablon e-mailu vyberte **+ nová šablona**. Vyberte typ e-mailu, pro který chcete vytvořit šablonu, vyberte příjemce, proces a událost, pro kterou musí být e-mail odeslán. Pak vyberte **Vytvořit**.

Šablona se otevře v zobrazení úprav a můžete ji pojmenovat. Předpokládejme například, že šablona je určena pro uchazeče z univerzity v USA, ale obsah je zapsaný ve francouzštině. V takovém případě můžete jako název zadat **Univerzita\_USA\_Francais**. Nadpis, řádek předmětu a obsah zprávy pro jakoukoli šablonu může kromě angličtiny podporovat jiné jazyky.

Pole **Komu** v šabloně nelze upravovat, protože příjemce je již vybrán při vytváření šablony.

Do řádku pro skrytou kopii (CC) můžete přidávat osoby jako **náborář** nebo **manažer náboru**. Při odeslání e-mailu jsou tyto role automaticky nahrazeny příslušnými uživateli na základě kontextu práce.

Řádek předmětu a obsah zprávy podporují zástupné symboly. Zástupné symboly můžete vkládat zadáním znaku **\#** a následným výběrem příslušného zástupného symbolu v rozevíracím seznamu automatického dokončování. Seznam dostupných zástupných symbolů se zobrazuje na pravé straně stránky. Po odeslání e-mailu jsou symboly automaticky nahrazeny na základě kontextu práce a příjemce. Zástupný text šablony e-mailu odesílaného uchazečům například obsahuje zástupný symbol \#{Candidate\_Name}. Při odesílání e-mailu uchazeči jménem Cameron bude tento zástupný symbol nahrazen jménem Cameron.

Editor obsahu zpráv je editor RTF umožňující vytvořit styl a formát textu. Umožňuje také vkládat hypertextové odkazy a ukotvení.

Po vytvoření šablony pro určitý typ e-mailu vyberte tlačítko se třemi tečkami (**...**) v řádku šablony a nastavte ji jako výchozí šablonu.

## <a name="consume-templates"></a>Používání šablon

Když náborový tým odešle e-mail, může používat šablony vytvořené správcem. Pokud bylo vytvořeno více šablon e-mailu, které uživatel odesílá, objeví se ve workflowu sestavování e-mailu rozevírací seznam. Výchozí šablona je zadána automaticky, ale uživatel může vybrat jinou šablonu.

> [!NOTE] 
> Pro automaticky odesílané e-maily můžete vytvořit více šablon. Pouze jednu šablonu však lze nastavit jako aktivní. Vzhledem k tomu, že tento proces spouštějí události, může pouze správce určit, která šablona se má použít, na základě kombinace odznaku **výchozí** a **Automaticky odeslané** v knihovně šablon.
