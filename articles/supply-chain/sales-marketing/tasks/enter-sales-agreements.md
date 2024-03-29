---
title: Zadávání prodejních smluv
description: Tento článek vysvětluje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b3aa72057753a9592fd47275dc996a3a904d86b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897480"
---
# <a name="enter-sales-agreements"></a>Zadávání prodejních smluv

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-sales-agreement-header"></a>Nastavení záhlaví prodejní smlouvy
1. V navigačním podokně přejděte na **Moduly > Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy**.
2. Zvolte **Nové**.
3. V poli **Účet odběratele** vyberte požadovaný záznam v rozevírací nabídce.
4. V poli **Klasifikace prodejní smlouvy** vyberte požadovaný záznam v rozevírací nabídce.
5. Rozbalte sekci **Obecné**.
6. V poli **Výchozí závazek** vyberte možnost **Závazek – hodnota produktu**. Typ závazku je povinné kritérium, které je nutné přiřadit ke smlouvě k definování způsobu plnění smlouvy. Čtyři přednastavené typy umožňují nastavit cíl závazku odběratele vyjádřený jako množství nebo hodnota. Typ závazku množství lze použít pouze k určitému produktu, ale oba typy hodnot se vztahují na prodej určeného a neurčeného zboží.  
7. Do pole **Datum vypršení platnosti** nastavte datum na budoucí datum, kdy má vypršet platnost smlouvy.
8. Vyberte **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Nastavení řádku závazku pro hodnotu produktu
1. Vyberte **Přidat řádek**.
2. V poli **Číslo položky** vyberte z rozevírací nabídky požadovaný záznam. Typ závazku, který jste vybrali pro smlouvu, ovlivňuje druh informací, které lze zadat na řádky smlouvy. Například u smlouvy založené na hodnotě je třeba určit celkovou čistou částku (v dohodnuté měně) za kterou se odběratel zavazuje koupit zboží od vás. V tomto příkladu nejsou pole **Množství** a **Jednotka** na řádku k dispozici vzhledem k tomu, že vytvoříte smlouvu pro zákazníka ke koupi produktu s konkrétní hodnotou.   
3. Do pole **Čistá částka** zadejte peněžní částku, za kterou se zákazník zavázal nakoupit.
4. Do pole **Procento slevy** zadejte procentuální hodnotu, která bude použita pro řádky prodejní objednávky odběratele, které jsou propojeny s touto smlouvou.
5. Rozbalte sekci **Podrobnosti řádku**.
6. Vyberte možnost **Ano** v poli **Max** je vynuceno.
    - Výběr možnosti **Max je vynuceno** znamená, že celková částka všech řádků prodejní objednávky používající zvláštní ceny závazku, slevy nebo platební podmínky, nesmí překročit částku zadanou v závazku.  
    - Minimální a maximální částky určují rozsah hodnot, za které musí být realizován prodej u jednotlivých prodejních objednávek používajících vybranou smlouvu.   
7. Rozbalte část **Záhlaví prodejní smlouvy**. Pokud je stav smlouvy nastaven na **Platná**, prodejní objednávky nesmí být přidruženy ke smlouvě a proto nemohou přispívat k plnění dohody. V této fázi lze stav změnit ručně. Stav by však normálně byl změněn při potvrzení smlouvy pro odběratele.  
8. V podokně akcí zvolte možnost **Prodejní smlouva**.
9. Vyberte **Potvrzení**. Ověřte, že možnost **Označit smlouvu jako platnou** je nastavena na hodnotu **Ano**.  
10. Vyberte možnost **Ano** v poli **Tisk sestavy**.
11. Vyberte **OK**.
12. Zavřete stránku. Smlouva je nyní platná. Můžete zahájit propojení smlouvy s objednávkami odběratele protiúčtem vůči potvrzenému cíli.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]