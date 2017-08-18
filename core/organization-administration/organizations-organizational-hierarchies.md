---
title: "Organizace a organizační hierarchie"
description: "Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4a7e1253d83e9212d423868a1f841b6944b07ad7
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="organizations-and-organizational-hierarchies"></a>Organizace a organizační hierarchie

[!include[banner](../includes/banner.md)]


Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.

<a name="organizations"></a>Organizace
-------------

V Microsoft Dynamics 365 for Finance and Operations můžete definovat následující typy interních organizací: právnické osoby, provozní jednotky a týmy.

Všechny interní organizace budou entita typu **Strana**. Proto tyto organizace používají adresáře k ukládání adres a kontaktních informací. Strana, což může být osoba nebo organizace, může patřit do jednoho nebo více adresářů.
### <a name="legal-entities"></a>Právnické osoby

Právnická osoba je organizace, která má registrovanou nebo uzákoněnou právní strukturu. Právnické osoby mohou uzavírat právní smlouvy a je po nich vyžadována příprava výkazů s informacemi o jejich výkonu. 

Společnost je typ právnické osoby. V této verzi Microsoft Dynamics Dynamics 365 for Finance and Operations jsou společnosti pouze druhem právnické osoby, kterou můžete vytvořit, a každá právnická osoba je spojena s identifikátorem společnosti. Toto přiřazení existuje vzhledem k tomu, že některé funkční oblasti v aplikaci používají ID společnosti nebo DataAreaId ve svých datových modelech. V těchto funkčních oblastech jsou společnosti používány jako hranice pro zabezpečení dat. Uživatelé mohou přistupovat k datům pouze pro společnost, ke které jsou aktuálně přihlášeni.

### <a name="operating-units"></a>Provozní jednotky

Provozní jednotka je organizace, která se používá k rozdělení řízení ekonomických zdrojů a operačních procesů v podniku. Osoby v provozní jednotce jsou povinni maximalizovat využívání omezených zdrojů, zdokonalovat procesy a zvažovat jejich výkon. 

Typy provozních jednotek v aplikaci Microsoft Dynamics Dynamics 365 for Finance and Operations zahrnují nákladová střediska, obchodní jednotky, hodnotové proudy, oddělení a maloobchodní kanály. V následující tabulce jsou uvedeny další informace o typech provozních jednotek.

| Typ provozní jednotky | Popis         | Účel      |
|---------------------|---------------------|--------------|
| Nákladové středisko         | Provozní jednotka, jejíž správci jsou odpovědní za rozpočtové a skutečné výdaje.                                                      | Slouží pro správu a provozní kontrolu obchodních procesů, které působí napříč právnickými osobami.                                         |
| Obchodní jednotka       | Částečně samostatná provozní jednotka vytvořená tak, aby naplňovala strategické obchodní cíle.                                                        | Používá se pro finanční vykazování podle průmyslových odvětví nebo produktových řad, které organizace nabízí nezávisle na právnických osobách. |
| Hodnotový proud        | Provozní jednotka, která řídí jeden nebo více výrobních toků.                                                                                  | Používané běžně v rámci lean manufacturing pro řízení aktivit a toků, které jsou požadovány pro dodávky produktu nebo služby spotřebitelům.  |
| Oddělení          | Provozní jednotka, která představuje kategorii nebo funkční část organizace, která provádí určitý úkol, například prodej nebo účetnictví. | Používané k vykazování ve funkční oblastech. Oddělení mohou mít odpovědnosti za zisk a ztráty a mohou obsahovat skupinu nákladových středisek.   |
| Maloobchodní síť      | Provozní jednotka, která představuje kamenný obchod, online obchod nebo online tržiště.                                          | Slouží pro správu a provozní kontrolu jednoho nebo více obchodů v rámci nebo napříč právnickými osobami.                                  |

### <a name="teams"></a>Týmy

Tým představuje organizaci, jejíž členové sdílejí společnou odpovědnost, zájem nebo cíl. V organizační hierarchii nelze použít týmy.

<a name="organizational-hierarchies"></a>Organizační hierarchie
--------------------------

Nastavení organizační hierarchie pro zobrazení a tvorbu sestav vašeho podnikání z různých perspektiv. Můžete například nastavit hierarchii pro právnické osoby pro daňové, právní nebo statutární vykazování. Nastavte hierarchii vycházející z provozní jednotky tak, aby vykazovala finanční informace, které nejsou vyžadovány zákonem, ale které se používají pro interní správu. Například můžete vytvořit hierarchii nákupu a řídit tak zásady nákupu, pravidla a obchodní procesy. 

Každé hierarchii je přiřazen účel v aplikaci Microsoft Dynamics Dynamics 365 for Finance and Operations. Účel hierarchie určuje typy organizací, které mohou být zahrnuty v hierarchii. Účel také určuje, v jakých scénářích aplikace lze hierarchii použít. 

Organizace v hierarchii mohou sdílet parametry, zásady a transakce. Organizace může dědit nebo přepsat parametry její nadřazené organizace. Sdílené hlavní data, například výrobky a adresáře, však platí pro celou organizaci, a nelze je přepsat pro jednotlivé organizace. Vytváření organizace a hierarchie vyžaduje pečlivé plánování. Další informace viz [Plánování organizační hierarchie](plan-organizational-hierarchy.md).






