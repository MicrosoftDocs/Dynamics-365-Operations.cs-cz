---
title: Pracovní prostor správy zaměstnaneckých výhod
description: Tento článek popisuje pracovní prostor správy zaměstnaneckých výhod v aplikaci Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 975b620dc911d154f6f67420a957bd72c02321ed
ms.sourcegitcommit: 6b013a423ed91973d60a895330046db2a07d92c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/12/2022
ms.locfileid: "9472706"
---
# <a name="benefits-management-workspace"></a>Pracovní prostor správy zaměstnaneckých výhod

Tento článek popisuje pracovní prostor **správy zaměstnaneckých výhod** v aplikaci Dynamics 365 Human Resources.

Pracovní prostor **Správa zaměstnaneckých výhod** poskytuje rychlý přehled o výhodách, které vyžadují vaši pozornost. Na této stránce uvidíte tyto údaje:

- Celkové počty položek čekajících na akci
- Pracovníci s nepotvrzenými výběry
- Pracovníci, kteří se nedávno přihlásili k zaměstnaneckým výhodám
- Pracovníci s budoucími životními událostmi
- Nově najatí zaměstnanci, kteří nejsou přihlášeni
- Pracovníci s aktivními životními událostmi
- Pracovníci s otevřenými zápisy, kteří si nevybrali žádné plány

![Pracovní prostor správy zaměstnaneckých výhod.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Zobrazení položek akcí

Položky akcí můžete zobrazit výběrem dlaždice nebo karty. Pokud vyberete kartu, můžete zobrazit a vybrat pracovníky přímo na stránce pracovního prostoru.

![Položky akcí.](./media/hr-benefits-management-workspace-action-items.png)

Pokud vyberete dlaždici, přejdete na stránku pro danou oblast. Například výběrem kterékoli z těchto dlaždic zobrazíte stránku **Plány zaměstnaneckých výhod**, ve které jsou vyfiltrováni zaměstnanci, u kterých musíte provést nějakou akci:

- **Nepotvrzené výběry**
- **Otevřené registrace bez rezervovaných plánů**
- **Zaregistrován k zaměstnaneckým výhodám**
- **Nový zaměstnanec nezaregistrován**

![Plány zaměstnaneckých výhod pracovníka.](./media/hr-benefits-management-workspace-plans.png)

Výběrem dlaždice **Aktivní životní události** nebo **Budoucí životní události** se přesunete na seznam aktivních nebo budoucích životních událostí.

![Životní události.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Zpracování

Chcete-li zpracovat způsobilost k registraci, životní události nebo aktualizace změn sazeb, vyberte příslušnou položku na navigačním panelu.

![Zpracovává se.](./media/hr-benefits-management-workspace-processing.png)

Chcete-li zobrazit výsledky procesu, vyberte možnost **Výsledky procesu**.

![Výsledky procesu.](./media/hr-benefits-management-workspace-process-results.png)

Další informace o zpracování výhod naleznete v tématu:

- [Zpracování způsobilosti k registraci](hr-benefits-process-enrollment-eligibility.md)
- [Zpracování změn životních událostí](hr-benefits-process-life-event-changes.md)
- [Zpracování způsobilosti k životním událostem](hr-benefits-process-life-event-eligibility.md)
- [Zpracování životních událostí](hr-benefits-process-life-events.md)
- [Zpracování změn sazby](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Změna období

Chcete-li zobrazit jiné období výhod, vyberte jej z rozbalovací nabídky **Období**.

![Změna období.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Karta Otevřená registrace

Položky akcí můžete zobrazit výběrem dlaždice nebo karty. Pokud vyberete kartu, můžete zobrazit a vybrat pracovníky přímo na stránce pracovního prostoru.
Karta **Otevřená registrace** poskytuje klíčové metriky pro proces otevřené registrace. 

Informace týkající se otevřené registrace se zobrazí 30 dní před **Počátečním datem přihlášení**. To je definováno v nastavení **Období** v dialogu **Správa výhod** > **Odkazy** > **Období** v poli **Počáteční datum přihlášení**.  Chcete-li toto nastavení změnit, přejděte na **Sdílené parametry lidských zdrojů** > **Správa výhod** > **Možnosti otevřené registrace** a aktualizujte pole **Počet**.  

Na kartě **Otevřená registrace** jsou k dispozici následující informace:
 - Zaměstnanci, kteří nezačali proces otevřené registrace
 - Zaměstnanci, kteří jsou v procesu voleb
 - Zaměstnanci, kteří dokončili proces voleb
 - Nepotvrzené výběry

**Dlaždice souhrnu**

- **Nezahájeno** – Dlaždice **Nezahájeno** zobrazuje počet zaměstnanců, kteří nezačali proces registrace. Dlaždice **Nezahájeno** je filtrovaný seznam, který zobrazuje pouze ty zaměstnance, kteří nemají pro období plánu otevřené registrace žádné plány vybrané, opuštěné ani rezervované. Povinné plány jsou ignorovány a nejsou zahrnuty, protože jsou ve výchozím nastavení pro zaměstnance vybrány.  Na této dlaždici můžete přejít zpět a zobrazit seznam zaměstnanců, kteří nezačali proces otevřené registrace na stránce **Plán zaměstnaneckých výhod**.

  > [!NOTE]
  > Pokud nechcete sledovat průběh otevřené registrace pro **Typ plánu**, můžete ho vyloučit tím, že přejdete na dialog **Správa výhod** > **Odkazy** > **Parametry samoobsluhy zaměstnance** > **Nastavení dlaždice plánu zaměstnaneckých výhod** a aktualizujete pole **Sledovat průběh otevřené registrace**.  Například můžete mít vytvořené plány, kde **Typ plánu** = **Jiný**. Tyto plány mohou být volitelnými plány, u kterých nechcete sledovat průběh registrace. Pokud tento typ plánu nevyberete, budou plány těchto typů na kartě **Otevřená registrace** ignorovány při sledování průběhu registrace nebo dokončení. Toto nastavení platí pro typ plánu, který je vybrán pro všechna období a právnické osoby.

- **Probíhá** – Dlaždice **Probíhá** udává počet zaměstnanců, u kterých probíhají volby. Dlaždice **Probíhá** je filtrovaný seznam, který zobrazuje pouze zaměstnance, kteří mají alespoň jeden opuštěný nebo vybraný plán. Povinné plány jsou ignorovány a nejsou zahrnuty, protože jsou ve výchozím nastavení pro zaměstnance vybrány. Z této dlaždice můžete přejít zpět a zobrazit vybrané a opuštěné plány na stránce **Hromadná aktualizace plánů zaměstnaneckých výhod**.

- **Zaregistrováno k zaměstnaneckým výhodám** – Dlaždice **Zaregistrováno k zaměstnaneckým výhodám** obsahuje počet zaměstnanců, kteří jsou plně registrováni k odběru výhod. Dlaždice **Zaregistrováno k zaměstnaneckým výhodám** je filtrovaný seznam, který zobrazuje zaměstnance, kteří buď vybrali všechny plány, nebo se všech plánů vzdali. Dotaz vyloučí plány, které nejsou sledovány kvůli otevřené registraci na stránce **Parametry samoobsluhy zaměstnance**. Z této dlaždice můžete přejít zpět a zobrazit seznam zaměstnanců na stránce **Plány zaměstnaneckých výhod**.

- **Nepotvrzené výběry** – Dlaždice **Nepotvrzené výběry** zobrazuje počet zaměstnanců, kteří mají plány, které jsou vybrány nebo se jich vzdali a je třeba je potvrdit. Z této dlaždice můžete přejít zpět a zobrazit stránku **Hromadná aktualizace plánů zaměstnaneckých výhod**.

**Aktivita**

- **Nezahájeno** – Dlaždice **Nezahájeno** zobrazuje seznam zaměstnanců, kteří nezačali proces registrace. Dlaždice **Nezahájeno** je filtrovaný seznam, který zobrazuje zaměstnance, kteří nemají pro období plánu otevřené registrace žádné plány vybrané, opuštěné ani rezervované. Povinné plány jsou ignorovány a nejsou zahrnuty, protože jsou ve výchozím nastavení pro zaměstnance vybrány. Můžete přejít na konkrétního pracovníka a zobrazit stránku **Podrobnosti plánů zaměstnaneckých výhod**.

- **Probíhající volby** – Karta **Probíhající volby** zobrazuje seznam zaměstnanců, u kterých probíhají volby. Dlaždice **Probíhající volby** je filtrovaný seznam, který zobrazuje pouze zaměstnance, kteří mají alespoň jeden opuštěný nebo vybraný plán. Povinné plány jsou ignorovány a nejsou zahrnuty, protože jsou ve výchozím nastavení pro zaměstnance vybrány. Můžete přejít na konkrétního pracovníka a zobrazit stránku **Podrobnosti plánů zaměstnaneckých výhod**.

## <a name="view-more-options"></a>Zobrazení dalších možností

Chcete-li zobrazit další informace anebo další akce, vyberte možnost **Odkazy**.

![Odkazy.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Viz také

[Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md)
