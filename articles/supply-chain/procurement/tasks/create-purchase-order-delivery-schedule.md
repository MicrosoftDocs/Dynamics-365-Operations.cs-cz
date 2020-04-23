---
title: Vytvoření nákupní objednávky s plánem dodávek
description: Toto téma ukazuje, jak vytvořit plán dodávek pro nákupní objednávku.
author: mkirknel
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e16c9adf592282a941b1112e197ea1ce9bdd34f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207708"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Vytvoření nákupní objednávky s plánem dodávek

[!include [banner](../../includes/banner.md)]

Toto téma ukazuje, jak vytvořit plán dodávek pro nákupní objednávku. Plán dodávek se používá, pokud množství z objednávky nebo deníku má být dodáno v podobě vícenásobné expedice. Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF. Tento postup by obvykle prováděl nákupčí.

## <a name="create-a-delivery-schedule"></a>Vytvoření plánu dodávek
1. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky**.
2. V podokně akcí vyberte **Nový**.
3. Do pole **Účet dodavatele** zadejte `US-101`.
4. Vyberte **OK**.
5. Do pole **Číslo položky** zadejte `M0001`.
6. Do pole **Množství** zadejte `10`.
7. Vyberte **Řádek nákupní objednávky**.
8. Vyberte **Plán dodávek**.
- Stránka **Plán dodávek** je místo, kde můžete zadat počet dodávek, ve kterých budou dodány celková množství řádku objednávky od dodavatele.  
- Ve výchozím stavu systém zkopíruje celkové množství a další podrobnosti o původním nákupním řádku na první řádek plánu dodávek. V tomto příkladu vytvoříme plán na dvě dodávky s posunem data druhé dodávky o týden od první.  
9. V poli **Množství** upravte množství na `4`.
10. Zvolte **Nové**.
11. V poli **Množství** zadejte zbývající množství `6`.
- V poli Datum dodání vyberte datum, které je týden po datu z prvního řádku dodávky.  
- Je možné sledovat celkové množství, která je přiděleno na řádky plánu dodávek tím, že si prohlédnete pole **Součet** a **Zbývající**. Pokud je zbývající množství nulové, bylo do plánu přiděleno celé množství z původního řádku.  
12. Rozbalte část **Převod nákladů**.
- Možnosti zde umožňují řídit způsob, jakým se náklady distribuují na řádcích plánu dodávek. Pokud vyberete **Kopírovat hrubé částky**, částka nákladů v původním řádku objednávky se zkopíruje do každého dodacího řádku. Možnost **Přidělit řádkům dodávek** rozděluje náklady z původního řádku podle množství na každém řádku dodávky.  
13. Sbalte část **Převod nákladů**.
14. Vyberte **OK**.
- Plán dodávek nyní byl použit v objednávce.  
- Původní řádek objednávky, nově označovaný jako obchodní řádek, byl předveden na řádek objednávky s více dodávkami. Je označen jedinečnou ikonou a funguje jako záhlaví pro řádky dodávky.  
15. Vyberte druhý řádek objednávky, který představuje první ze dvou řádků dodávky.
- Dva nové řádky označované jako řádky dodávky tvoří jeden plán dodávek. Objednávka bude zpracována s ohledem na tyto řádky, nikoli na původní řádek. Pokud jsou vytištěny dokumenty, jako například potvrzení, deníky příjemek produktu nebo faktury, budou zobrazeny pouze řádky dodávky.  

## <a name="change-the-delivery-schedule"></a>Upravte plán dodávek
Množství na dodacích řádcích lze změnit. Pokud to provedete, aktualizuje se automaticky obchodní řádek o celkové množství z řádků dodávky.  
1. Do pole **Množství** na prvním řádku dodávky změňte množství ze `4` na `5`.
2. Vyberte první řádek objednávky (obchodní řádek).  
- Množství na obchodním řádku bylo změněno na 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Zpracování příjmu produktu pomocí plánů dodávek
Nákupní objednávka musí být potvrzena, než bude možné zpracovat příjemku produktu. V tomto případě je příjem zaznamenán přímo v nákupní objednávce. Příjem může také byly zaznamenány při příjmu zboží ve skladu.  
1. V podokně akcí klikněte na možnost **Zakoupit**.
2. Vyberte **Potvrdit**.
3. V podokně akcí klikněte na možnost **Přijmout**.
4. Vyberte **Příjemka produktu**. Do pole **Příjemka produktu** zadejte libovolnou hodnotu.
- Toto pole slouží k zadání reference, která bude použita jako doklad pro deník příjemek produktů.  
- V poli **Množství** vyberte **Objednané množství**. Tato možnost znamená, že se během příjmu zpracuje množství, se kterým byly řádky objednávky vytvořeny.  
- Ujistěte se, že pole **Vytisknout příjemku produktu** je nastaveno na hodnotu **Ne**. V tomto příkladu není třeba provádět tisk.  
5. Rozbalte sekci **Řádky**.
- Všimněte si, že je vytvořena příjemka produktu pro dva řádky dodávky, ale ne pro původní řádek objednávky. Pokud byl zaznamenán příjem ve skladu, byl také zaznamenán na řádcích plánu dodávky.  
6. Sbalte oddíl **Řádky**.
7. Výběrem tlačítka **OK** zaúčtujte příjem.

