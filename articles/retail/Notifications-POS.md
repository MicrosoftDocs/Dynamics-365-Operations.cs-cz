---
title: "Zobrazení oznámení objednávek v pokladním místě"
description: "Toto téma popisuje postup povolení oznámení objednávek v pokladním místě a architekturu oznámení, kterou lze rozšířit na další operace."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: a1206aea3f78246951581c1dc6338e39a0942ea2
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="display-notifications-in-point-of-sale"></a>Zobrazení oznámení v pokladním místě

[!include[banner](includes/banner.md)]

V dnešním moderním prostředí maloobchodu jsou zaměstnancům obchodu přiřazovány různé úkoly, jako je pomoc zákazníkům, zadávání transakcí, provádění inventur a přijímání objednávek v obchodě. Klient POS umožňuje zaměstnancům provádět tyto a mnohé další úlohy v jedné jediné aplikaci. Kvůli různým úlohám prováděným během dne může být pro zaměstnance nutné dostávat oznámení, pokud cokoliv vyžaduje jejich pozornost. Architektura oznámení v POS řeší tento problém tím, že maloobchodní prodejci mohou nakonfigurovat oznámení na základě rolí. U aplikace Dynamics 365 for Retail s aktualizací Application update lze tato oznámení konfigurovat pouze pro POS operace.

V současné době systém poskytuje možnost zobrazit oznámení pro operaci plnění objednávky, architektura je však navržena tak, aby byla rozšířitelná, aby v budoucnu mohli vývojáři psát obslužné rutiny oznámení pro jakoukoliv operaci a zobrazit oznámení v POS.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Povolení oznámení pro operace plnění objednávky

Chcete-li povolit oznámení pro operace plnění objednávky, postupujte podle následujících kroků:

 - Přejděte na stránku **Operace** (**Maloobchodní prodej** > **Nastavení kanálu** > **Nastavení POS** > **POS** > **Operace**).
 - Vyhledejte Operace plnění objednávky a vyberte zaškrtávací políčko **Povolit oznámení** pro tuto operaci. To označí architektuře oznámení, aby naslouchala obslužné rutině pro operaci plnění objednávky. Je-li implementována obslužná rutina, oznámení se zobrazí v POS, v opačném případě nebudou pro tuto operaci oznámení zobrazena.
- Přejděte na oprávnění POS přidružená k zaměstnancům a na pevné záložce **Oznámení** přidejte operaci plnění objednávky s pořadím zobrazení 1. Pokud je nakonfigurováno více než jedno oznámení , pořadí zobrazení se používá k uspořádání oznámení odshora dolů s hodnotou 1 nahoře. Lze přidat pouze ty operace, pro které bylo zvoleno zaškrtávací políčko **Povolit oznámení**. Kromě toho se zobrazí oznámení pouze pro ty operace, které byly přidány zde, a pouze těm pracovníkům, kterým byly operace přidány k příslušným POS oprávněním. 

> [!NOTE]
> Oznámení můžete přepsat na úrovni uživatele přechodem do záznamu pracovníka a výběrem **Oprávnění POS** a následnou úpravou oznámení pro tohoto uživatele.

 - Přejděte na stránku **Funkční profil** (**Maloobchodní prodej** > **Nastavení kanálu** > **Nastavení POS** > **Profily POS** > **Funkční profily**). Aktualizujte vlastnost **Interval oznámení** pro nastavení intervalu v minutách, ve kterém mají být notifikace odesílány. Doporučujeme nastavit tuto hodnotu na 10 minut, abyste se vyhnuli nadměrné komunikaci s ústředím. Nastavení intervalu oznámení na hodnotu 0 vypne oznámení.  

 - Přejděte do **Maloobchodní prodej** > **Maloobchodní IT** > **Distribuční plán**. Vyberte plán „1060, Zaměstnanci“ za účelem synchronizace nastavení odběru oznámení a poté klikněte na **Spustit**. Dále synchronizujte interval výběrem položky „1070, Konfigurace kanálu“ a poté klikněte na **Spustit**. 

## <a name="view-notifications-in-pos"></a>Zobrazení oznámení v POS

Po dokončení výše uvedených kroků mohou pracovníci, pro které jsou nastavena oznámení, zobrazit oznámení v POS. Chcete-li zobrazit oznámení, klikněte na ikonu oznámení v záhlaví POS. Zobrazí se centrum oznámení s oznámeními pro operaci plnění objednávky. Centrum oznámení má zobrazit následující skupiny v rámci operace plnění objednávky: 

- **Čekající objednávky** – Tato skupina zobrazuje počet objednávek ve stavu čekání, jako například objednávky, které je třeba přijmout pracovníkem POS, který má požadovaná oprávnění pro plnění obchodu. Kliknutím na počet na skupině otevře stránku **Plnění objednávky**, vyfiltrovanou pro zobrazení pouze čekajících objednávek přiřazených k obchodu pro plnění. Pokud jsou objednávky přijaty automaticky pro obchod, bude počet pro tuto skupinu nula.

- **Vyzvednutí v obchodě** -Tato skupina zobrazí počet objednávek, které mají způsob dodání **Výdej** a vyskladnění je naplánováno z aktuálního obchodu. Kliknutím na počet na skupině otevře stránku **Plnění objednávky**, vyfiltrovanou pro zobrazení aktivních objednávek, které jsou nastaveny k vyzvednutí z aktuálního obchodu.

- **Expedovat z obchodu** -Tato skupina zobrazí počet objednávek, které mají způsob dodání **Expedice** a expedice je naplánována z aktuálního obchodu. Kliknutím na počet na skupině otevře stránku **Plnění objednávky**, vyfiltrovanou pro zobrazení aktivních objednávek, které jsou nastaveny k expedici z aktuálního obchodu.

Pokud existují nové objednávky přiřazené k obchodu pro plnění, změní se ikona oznámení za účelem označení, že budou aktualizována nová oznámení a počet odpovídajících skupin. Uživatel může také kliknout na ikonu obnovení, vedle názvu operace, aby se okamžitě aktualizoval počet skupin. Počet bude aktualizován také v předdefinovaných intervalech. Jakákoliv skupina s novou položkou, která se nezobrazuje aktuálnímu pracovníkovi, zobrazí ikonu výbuchu označující, že tato skupina má novou položku. Kliknutí na dlaždice v rámci oznámení otevře konkrétní operaci, pro kterou je oznámení nakonfigurováno. Ve výše uvedených scénářích otevře kliknutí na oznámení stránku **Plnění objednávky** a předá příslušné parametry: čekající objednávky, vyzvednutí v obchodě a expedice z obchodu. 

> [!NOTE]
> Oznámení o čekajících objednávkách budou povolena v následující aktualizaci aplikace Dynamics 365 for Retail. 


