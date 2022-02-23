---
title: Export data z aplikací Attract a Onboard
description: Export data z aplikací Dynamics 365 Talent - Attract a Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460512"
---
# <a name="export-data-from-attract-and-onboard"></a>Export data z aplikací Attract a Onboard

[!include [banner](includes/banner.md)]

Jak bylo ohlášeno v tématu [Vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), 1. února 2022 proběhne vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard. Chcete-li pomoci s migrací na jiný produkt, obě aplikace nyní poskytují možnosti exportu dat.

## <a name="export-data-from-attract"></a>Exportovat data z aplikace Attract

Data můžete exportovat bez omezení přístupu k prostředí. Tuto akci lze provést pro účely testování nebo pro pochopení struktury dat. Až budete připraveni na migraci, omezte přístup k prostředí Attract podle pokynů v tomto postupu. Nezapomeňte data exportovat znovu. 

1. Přejděte na [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. V části **Export dat** vyberte **Požádat o export dat**.

   ![[Žádost o export data z aplikace Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Jakmile se objeví zpráva **Váš požadavek se zpravovává**, vyberte **OK**. Export dat může trvat až 20 minut, v závislosti na velikosti exportu.

4. Po dokončení exportu vyberte tlačítko vedle **Stáhnout**. 

   >[!NOTE]
   >Všechny exporty dat jsou k dispozici po dobu sedmi dnů, kdy vyprší platnost odkazu pro **Stažení**.</br>
   
Stahování obsahuje soubor. zip s daty Attract včetně následujících složek:

| Název složky | Popis |
| --- | --- |
| Nastavení pro správu | Konfigurace centra správy Attract. |
| Kandidáti | Všichni kandidáti, kteří byli přidáni do projektů nebo fondů talent. |
| Šablony e-mailů | Všechny e-mailové šablony, které byly nakonfigurovány pro prostředí. |
| Šablony balíčku nabídky práce | Všechny vytvořené šablony balíků nabídek práce spolu s přidruženými konfiguracemi. |
| Sady pravidel nabídek práce |  Všechny soubory sady pravidel, které byly odeslány pro správu nabídek. |
| Šablony nabídky práce | Všechny šablony dokumentů nabídek práce jsou vytvořeny pro prostředí. |
| Volná pracovní místa | Všechna vytvořená pracovní místa. Odstraněné práce nejsou exportovány. Podsložky obsahují kandidátské žádosti, u nichž jsou dílčí složky pro přílohy kandidáta aplikace a balíčky nabídek, kde je to vhodné. |
| Šablony volných pracovních míst | Šablony procesů nabídek práce, které byly nakonfigurovány v prostředí. |
| Skupiny talentů | Všechny vytvořené skupiny talentů, jejich seznamy přispěvatelů a seznamy kandidátů pro skupiny talentů. |
| Pracovníci | Seznam všech pracovníků přítomných v prostředí a jejich rolí. |
| (kořenová složka) | Soubor schématu JSON, který popisuje pole struktury dat. |

### <a name="restrict-access-to-attract"></a>Omezit přístup k Attract

Jakmile budete připraveni na migraci, omezte přístup uživatelů, kteří nepatří k prostředí Attract, a exportujte data.

>[!IMPORTANT]
>Omezení přístupu k prostředí Attract je trvalé a nelze je vrátit zpět. Chcete-li pokračovat v přístupu k prostředí, můžete tento krok přeskočit.

1. Přejděte na [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Chcete-li omezit přístup nesprávců k vašemu prostředí Attract v rámci **Omezení přístupu k této aplikaci**, vyberte **Omezit přístup nyní**. Omezením přístupu také zmizí všechny aktivní nabídky práce, které byly zveřejněny.

   ![[Omezit přístup nesprávců k Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Pokud se zobrazí upozornění **Jedná o trvalou změnu změnu**, vyberte **Omezit přístup** k trvalému omezení přístupu uživatelů bez oprávnění správce do tohoto prostředí. Nejste-li připraveni dokončit tento krok, vyberte možnost **Storno**.

   ![[Upozornění, že omezení přístupu je trvalá změna](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Správci mohou po omezení přístupu k prostředí Attract i nadále přistupovat ke stránkám exportu dat a sestav osob.

## <a name="export-data-from-onboard"></a>Exportovat data z aplikace Onboard

Až budete připraveni, můžete stáhnout šablony, příručky a data kandidátý z Onboard.

1. Přejděte na [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. V části **Export dat** vyberte **Požádat o export dat**. 

   ![[Žádost o export data z aplikace Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Jakmile se objeví zpráva **Váš požadavek se zpravovává**, vyberte **OK**. Export dat může trvat až 20 minut, v závislosti na velikosti exportu.

4. Po dokončení exportu vyberte tlačítko vedle **Stáhnout**. 

   ![[Stáhnout export dat z aplikace Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Export dat je k dispozici po sedm dní. Po sedmi dnech vyprší platnost odkazu **Stažení** a je nutné požádat o nový export v případě, že je nutné data stáhnout znovu. Když spustíte nový export dat, platnost stávajících stahování skončí po úspěšném dokončení nového exportu.

Stahování je soubor zip, který obsahuje:

- Složku **Šablony**, která obsahuje šablony Onboard ve formátu dokumentu aplikace Word.

- Složku **Průvodci**, která obsahuje průvodce Onboard ve formátu dokumentu aplikace Word.

## <a name="see-also"></a>Viz také

[Vyřazení aplikací Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)