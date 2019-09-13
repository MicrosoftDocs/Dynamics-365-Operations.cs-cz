---
title: Nastavení preferovaných pracovníků údržby
description: Toto téma vysvětluje, jak nastavit preferované pracovníky údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887404"
---
# <a name="preferred-maintenance-workers"></a>Preferovaní pracovníci údržby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Můžete vytvořit předvolbu, která se týká pracovníků údržby přidělených k dokončení pracovních příkazů během plánování pracovních příkazů. Použití této funkce je volitelné, ale může vám pomoci vybrat pro nejvíce kvalifikovaného pracovníka údržby, aby dokončil úlohu na základě dovedností a kompetencí pracovníků. V průběhu plánování pracovních příkazů lze tedy pomocí nastavení **Preferovaní pracovníci údržby** určit, zda má být pro pracovní příkaz naplánován určitý pracovník údržby nebo skupina pracovníků. Naplánovány budou pouze pracovníci údržby, kteří jsou k dispozici v čase plánování. Pokud je nastavení preferovaných pracovníků údržby během plánování shodné s pracovním příkazem, ale pracovník údržby je přidělen k jiným úlohám, bude pracovní příkaz naplánován na jiného dostupného pracovníka údržby.

Před nastavením preferovaných pracovníků údržby je nutné nejprve nastavit pracovníky údržby a skupiny pracovníků, kteří by měli být k dispozici pro výběr. Informace o tom, jak nastavit pracovníky údržby a skupin pracovníků, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Nastavení preferovaných pracovníků

Upřednostňovaný pracovník údržby nebo skupina pracovníků může souviset s konkrétní

- obchod  
- variantou typu práce údržby  
- typ práce údržby  
- kategorie typu práce údržby  
- majetek  
- typ majetku  

nebo kombinaci těchto výběrů. Čím více výběrů, které provedete pro stejný záznam, tím přesnější bude nastavení.

1. Klikněte na **Správa majetku** > **Nastavení** > **Pracovníci** > **Preferovaní pracovníci údržby**.

2. Kliknutím na možnost **Nový** vytvořte nový záznam.

3. Začněte vytvořením „výchozího“ pracovníka pro údržbu nebo nastavení skupiny pracovníků, který nemá žádné výběry v polích zobrazených v předchozím seznamu odrážek. To znamená, že provedete výběr pouze v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**. Na níže uvedeném obrázku vidíte příklad v prvním záznamu, ve kterém je vybrána možnost „požadavky“ jako skupina preferovaných pracovníků údržby.

>[!NOTE]
>Toto výchozí nastavení bude použito během plánování pracovního příkazu, pokud žádná jiná specifická kombinace neodpovídá obsahu pracovního příkazu během plánování pracovního příkazu.

4. Opakujte krok 2 a vytvořte nový záznam. Proveďte požadované výběry v závislosti na úrovni podrobností pro preferovaného pracovníka nebo skupinu pracovníků. *Příklad:* na obrázku níže, v šestém záznamu, je jako preferovaný pracovník vybrán pracovník údržby Shawn Richardson. Při plánování pracovního příkazu bude automaticky vybrána možnost, která zahrnuje majetek CH-BP1-03-02 a typ práce údržby "Hodnocení zařízení", pokud je k dispozici v naplánovaném čase.

>[!NOTE]
>Obecně platí, že když je při plánování pracovních příkazů vybrán preferovaný pracovník údržby, Správa majetku projde všechny záznamy **Preferovaní pracovníci údržby** a zkontroluje možné odpovídající položky. Vždy nejprve zkontroluje nejkonkrétnější kombinaci. Pokud není nalezena žádná shoda, bude použit "výchozí" záznam s výběrem v poli **Skupina preferovaných pracovníků údržby** nebo **Preferovaný pracovník údržby**.


![Obrázek č. 1](media/02-work-order-scheduling.png)

Můžete také nastavit odpovědné pracovníky údržby, kteří mohou být vybráni při vytvoření požadavku na údržbu nebo pracovního příkazu. Ve **Všech pracovních příkazech** a **Všech požadavcích na údržbu** můžete výběr v případě potřeby upravit. Další informace naleznete v sekci [Odpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).

Při plánování pracovních příkazů se počítají různé výsledky s cílem určit, kteří pracovníci by měli dokončit úlohy související s pracovním příkazem (tato skóre se nastavují v nabídce **Parametry správy majetku** > **Plánování pracovních příkazů**). Pokud při plánování pracovních příkazů získají dva nebo více preferovaných pracovníků údržby nebo odpovědných pracovníků údržby stejné hodnocení, bude jeden pracovník vybrán náhodně. V opačném případě je vždy pracovník s nejvyšším skóre přidělen k dokončení pracovního příkazu.

