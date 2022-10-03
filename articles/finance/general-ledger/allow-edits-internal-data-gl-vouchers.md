---
title: Povolit úpravy interních dat v dokladech hlavní knihy
description: Tento článek poskytuje informace o tom, jak upravit interní data na dokladech hlavní knihy.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573244"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Povolit úpravy interních dat v dokladech hlavní knihy

[!include[banner](../includes/banner.md)]


Když zaúčtujete účetní zápisy do hlavní knihy, pole **Popis** se často používá k ukládání interních poznámek nebo dokumentace. Pokud jsou informace nesprávné, může to způsobit zmatek a ztížit uzávěrku období. Tato funkce umožňuje vedoucímu účetnictví nebo nadřízenému účetnictví opravit chyby úpravou pole **Popis** na zaúčtovaných dokladech v hlavní knize.

Změny zaúčtovaných dokladů v hlavní knize jsou omezeny na data, která mají interní povahu. Tato funkce vám nikdy neumožní upravovat data, jako jsou částky, data účtování, účty hlavní knihy a měna transakce. Změny těchto údajů ovlivní externí vykazování účetní závěrky a musí být provedeny pouze prostřednictvím nových dokladů hlavní knihy.

> [!NOTE]
> U Dynamics 365 Finance verze 10.0.29 je tato funkce omezena na úpravy pole **Popis**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Úprava interních dat v dokladech hlavní knihy

Než bude možné upravovat interní data na dokladech hlavní knihy, musíte aktivovat funkci **Povolit úpravy interních dat na dokladech hlavní knihy** v pracovním prostoru **Správa funkcí**.
Po aktivaci funkce musí být uživatel, který bude upravovat zaúčtované poukázky, přiřazen k roli vedoucího účetnictví nebo nadřízeného účetnictví. Oprávnění můžete přidat i k dalším rolím, a to přizpůsobením rolí zabezpečení.

Proces úprav je povolen pouze ze stránky Transakce dokladu.

1. Přejděte na **Hlavní kniha** > **Dotazy a sestavy** > **Transakce dokladu**.
2. V dialogovém okně **SysQuery** zadejte vyhledávací kritéria pro výběr dokladů.
3. Vyberte řádky pro doklady, které chcete upravit, a pak vyberte **Upravit doklad** > **Upravit interní údaje dokladu**.

    [![Stránka transakcí dokladu.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Na stránce **Upravit interní údaje dokladu** se pro každý vybraný řádek zobrazí následující údaje:
  
  - Účet hlavní knihy
  - Název účtu
  - Doklad
  - Aktuální popis
  - Nový popis

    [![Doklad deníku.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Lze upravit pouze pole **Nový popis**. Ve výchozím nastavení se hodnota shoduje s hodnotou pole **Aktuální popis**, abyste mohli rychle opravit drobné chyby v popisu.

4. Upravte pole **Nový popis** na každém řádku nebo odstraňte popis z každého řádku.

   Případně, pokud je třeba aktualizovat více řádků stejnou hodnotou, postupujte takto:

      1. Vyberte řádky, které chcete upravit, a poté vyberte **Hromadně aktualizovat vybrané záznamy**.
      2. V poli **Pole k úpravě** vyberte pole, které chcete upravit. V současné době vyhledávání zahrnuje pouze pole **Nový popis**.
      3. Do pole **Nová hodnota** zadejte nový popis.
      4. Vyberte **Aktualizovat**. Všechny vybrané záznamy se aktualizují novou hodnotou.

      [![Dialogové okno Hromadně aktualizovat vybrané záznamy.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Do pole **Důvod úpravy** zadejte poznámku vysvětlující, proč byla úprava provedena. Tato poznámka je zobrazena na stránce **Záznam úprav dokladů pro audit**.

   Na stejném dokladu lze provést více úprav a každá úprava bude sledována.

## <a name="audit-trail-of-voucher-edits"></a>Auditní záznam úprav dokladů

Záznam pro audit je udržován speciálně pro sledování změn provedených prostřednictvím této funkce. K záznamu pro audit úprav dokladů můžete přistupovat dvěma způsoby:

  - Přejděte na **Hlavní kniha** > **Dotazy a sestavy** > **Transakce dokladu**. Na stránce **Dotazy na doklady** vyberte **Upravit doklad** > **Záznam pro audit úprav dokladů**. Záznam pro audit se zobrazí pouze pro vybraný záznam dokladu. 
   
    Otevřením dotazu tímto způsobem se můžete zaměřit na všechny úpravy, které byly provedeny v jednom záznamu dokladu.
  
  - Přejděte na **Hlavní kniha** > **Periodické úkoly** > **Záznam pro audit úprav dokladů**. V dialogovém okně zadejte kritéria pro určení dokladů, pro které chcete zobrazit záznam pro audit. Chcete-li zobrazit záznam pro audit pro všechny doklady, ponechte kritéria prázdná a vyberte **OK**. 
    
    Otevřením dotazu tímto způsobem můžete filtrovat úpravy, které byly provedeny ke konkrétnímu datu nebo konkrétním uživatelem.

Stránka **Záznam pro audit úprav** zobrazuje následující informace:

- **Datum a čas vytvoření** – Datum a čas úpravy.
- **Důvod úpravy** – Důvod, který uživatel zadal pro úpravu.
- **Vytvořil(a)** – Uživatel, který úpravu provedl.

Chcete-li zobrazit údaje každého záznamu pro audit, přejděte na hodnotu **Datum a čas vytvoření**. Stránka **Zobrazit upravené vlastnosti dokladu** zobrazuje stejné informace jako původní stránka úprav, včetně předchozího popisu a aktualizovaného popisu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
