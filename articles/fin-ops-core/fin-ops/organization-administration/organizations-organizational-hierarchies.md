---
title: Přehled organizací a organizačních hierarchií
description: Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.
author: sericks007
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efd34b01ab414b2282fd08d8d9329ae7f9a801ce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747628"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Přehled organizací a organizačních hierarchií

[!include [banner](../includes/banner.md)]

Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.

## <a name="organizations"></a>Organizace

Můžete definovat následující typy interních organizací: právnické osoby, provozní jednotky a týmy.

Všechny interní organizace budou entita typu **Strana**. Proto tyto organizace používají adresáře k ukládání adres a kontaktních informací. Strana, což může být osoba nebo organizace, může patřit do jednoho nebo více adresářů.

### <a name="legal-entities"></a>Právnické osoby

Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu. Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu.

Společnost je typ právnické osoby. V současné době jsou společnosti pouze druhem právnické osoby, kterou můžete vytvořit, a každá právnická osoba je spojena s identifikátorem společnosti. Toto přiřazení existuje vzhledem k tomu, že některé funkční oblasti v aplikaci používají ID společnosti nebo DataAreaId ve svých datových modelech. V těchto funkčních oblastech jsou společnosti používány jako hranice pro zabezpečení dat. Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni.

### <a name="operating-units"></a>Provozní jednotky

Provozní jednotka je organizace, která se používá k rozdělení řízení ekonomických zdrojů a operačních procesů v podniku. Osoby v provozní jednotce jsou povinni maximalizovat využívání omezených zdrojů, zdokonalovat procesy a zvažovat jejich výkon.

K typům provozních jednotek patří nákladová střediska, obchodní jednotky, hodnotové proudy, oddělení a velkoobchodní kanály. V následující tabulce jsou uvedeny další informace o typech provozních jednotek.

| Typ provozní jednotky | Popis | Účel |
|---------------------|-------------|---------|
| Nákladové středisko         | Provozní jednotka, jejíž správci jsou odpovědní za rozpočtové a skutečné výdaje. | Slouží pro správu a provozní kontrolu obchodních procesů, které působí napříč právnickými osobami. |
| Obchodní jednotka       | Částečně samostatná provozní jednotka vytvořená tak, aby naplňovala strategické obchodní cíle. | Používá se pro finanční vykazování podle průmyslových odvětví nebo produktových řad, které organizace nabízí nezávisle na právnických osobách. |
| Hodnotový proud        | Provozní jednotka, která řídí jeden nebo více výrobních toků. | Používané běžně v rámci lean manufacturing pro řízení aktivit a toků, které jsou požadovány pro dodávky produktu nebo služby spotřebitelům. |
| Oddělení          | Provozní jednotka, která představuje kategorii nebo funkční část organizace, která provádí určitý úkol, například prodej nebo účetnictví. | Používané k vykazování ve funkční oblastech. Oddělení mohou mít odpovědnosti za zisk a ztráty a mohou obsahovat skupinu nákladových středisek. |
| Kanál pro velkoobchod      | Provozní jednotka, která představuje kamenný obchod, online obchod nebo online tržiště. | Slouží pro správu a provozní kontrolu jednoho nebo více obchodů v rámci nebo napříč právnickými osobami. |

### <a name="teams"></a>Týmy

Tým představuje organizaci, jejíž členové sdílejí společnou odpovědnost, zájem nebo cíl. V organizační hierarchii nelze použít týmy.

## <a name="organizational-hierarchies"></a>Organizační hierarchie

Nastavení organizační hierarchie pro zobrazení a tvorbu sestav vašeho podnikání z různých perspektiv. Můžete například nastavit hierarchii pro právnické osoby pro daňové, právní nebo statutární vykazování. Nastavte hierarchii vycházející z provozní jednotky tak, aby vykazovala finanční informace, které nejsou vyžadovány zákonem, ale které se používají pro interní správu. Například můžete vytvořit hierarchii nákupu a řídit tak zásady nákupu, pravidla a obchodní procesy.

Každé hierarchii je přiřazen účel. Účel hierarchie určuje typy organizací, které mohou být zahrnuty v hierarchii. Účel také určuje, v jakých scénářích aplikace lze hierarchii použít.

Organizace v hierarchii mohou sdílet parametry, zásady a transakce. Organizace může dědit nebo přepsat parametry její nadřazené organizace. Sdílené hlavní data, například výrobky a adresáře, však platí pro celou organizaci, a nelze je přepsat pro jednotlivé organizace. Vytváření organizace a hierarchie vyžaduje pečlivé plánování. Další informace viz [Plánování organizační hierarchie](plan-organizational-hierarchy.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]