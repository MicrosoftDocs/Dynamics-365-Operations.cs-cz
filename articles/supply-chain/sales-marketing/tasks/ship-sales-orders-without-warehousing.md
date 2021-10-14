---
title: Expedování prodejních objednávek bez skladování
description: Toto téma vysvětluje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10e21bcdef22caf4f4d97ba7dd36ebf1a6e6e055
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578865"
---
# <a name="ship-sales-orders-without-warehousing"></a>Expedování prodejních objednávek bez skladování

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli. Průvodce lze použít pro tok plnění, který není nastaven pro správu skladu (ani základní ani rozšířené funkce skladu), a proto nevyžaduje zaregistrování výdeje produktu mají před dodávkou. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. V obou případech před spuštěním této úlohy vytvořte prodejní objednávku pro produkt na skladě s množstvím větším než 1. Abyste předešli chybě zaúčtování, je třeba zkontrolovat, že množství produktu na skladě na pracovišti a ve skladu, které jste vybrali na objednávce, zahrnuje množství objednávky.

## <a name="post-packing-slip-for-an-order"></a>Zaúčtování dodacího listu pro objednávku
1. V navigačním podokně přejděte na **Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. V seznamu vyhledejte a vyberte objednávku, kterou jste vytvořili pro tento úkol.
3. V podokně akcí vyberte **Vyskladnit a zabalit**.
4. Vyberte **Zaúčtovat dodací list**.
5. Rozbalte nebo sbalte oddíl **Parametry**.
6. V poli **Množství** vyberte možnost **Vše**.
    - Ostatní možnosti zahrnují **Dodat nyní** a **Vyskladněno**. Pokud řádek objednávky má být částečně dodán a pole **Dodat nyní** v řádku objednávky obsahuje nějaké množství, vybrali byste **Dodat nyní**. Pokud tok plnění vaší organizace zahrnuje výdej jako samostatný proces, který je spravován a zaregistrován ve výdejce, měli byste vybrat **Vyskladněno**.  
    - Zkontrolujte, zda je možnost **Zaúčtování** nastavena na hodnotu **Ano**.  
7. Nastavte možnost **Tisk dodacího listu** na **Ano**. Karta **Přehled** obsahuje seznam dodacích listů k vygenerování v tomto zaúčtování. Pokud dodáváte jednotlivé objednávky, obvykle bude jeden dodací list. Avšak jsou-li řádky objednávky, která má být expedována, z různých pracovišť, zaúčtování bude automaticky rozděleno na příslušný počet dokumentů. Jedná se o povinnou podmínku, kterou nelze změnit. Obdobně platí, že zaúčtování bude rovněž rozděleno do několika dokumentů, pokud mají řádky objednávky k dodání různé doručovací adresy a nastavení zásad expedice vyžaduje rozdělení.  
8. Na kartě **Řádky** vyberte řádek pro řádek objednávky k expedici.
9. V poli **Aktualizace** zadejte číslo menší než původní množství.
10. Vyberte **OK**.
11. Vyberte **Ano**.
12. Zavřete stránku.
13. V podokně akcí vyberte **Možnosti**.
14. Vyberte **Změnit zobrazení**.
15. Vyberte **Zobrazení záhlaví**.
    - Pokud byly plně expedovány všechny řádky objednávky, stav zakázky se změní z otevřeného na dodáno.  
    - V tomto případě byl řádek objednávky expedován částečně. Toto je důvod, proč stav objednávky zůstane otevřený.     
    - Pole **Stav dokumentu** je nastaveno na Dodací list, protože alespoň jeden z řádků objednávky byl dodán.  
16. V podokně akcí klikněte na možnost **Obecné**.
17. Vyberte **Množství řádků**.
18. Zavřete stránku.
19. V podokně akcí vyberte **Vyskladnit a zabalit**.
20. Vyberte **Dodací list**. Stránka **Deník dodacích listů** obsahuje všechny dokumenty dodacího listu, které byly vygenerovány pro vaši objednávku. Můžete zkontrolovat podrobnosti o jednotlivých dokumentech a vytisknout je, pokud chcete.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]