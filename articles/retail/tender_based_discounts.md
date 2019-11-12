---
title: Slevy založené na úhradě
description: V tomto tématu je uveden přehled funkcí, které prodejcům umožňují konfigurovat specifické typy úhrad.
author: bebeale
manager: AnnBe
ms.date: 10/25/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 245ee647a3b86303df046fda5bba406c7a2485b5
ms.sourcegitcommit: b0c176d5d24939307c6d0a6dbe7656007ca53710
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2019
ms.locfileid: "2673558"
---
# <a name="tender-based-discounts"></a>Slevy založené na úhradě

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Jedná se o běžný postup v rámci maloobchodních prodejců při uvolňování soukromých kreditních karet. Maloobchodní prodejci z toho mají prospěch, protože získají upřednostňované sazby od bank. Vzhledem k tomu, že tyto kreditní karty mohou zákazníky povzbudit k častějším návštěvám obchodu, pomáhají zlepšit hlavní řádek maloobchodníka. Maloobchodníci proto mají motivaci ke zvýšení zákaznických kreditních karet. Když chtějí dosáhnout tohoto cíle, často poskytují zákazníkům, kteří tyto kreditní karty používají, další slevy.

Maloobchodníci, kteří neposkytují kreditní karty, mohou například případně požadovat, aby zákazníci zaplatili pomocí jiných typů úhrad, jako jsou hotovost, dárkové poukazy nebo věrnostní body. Tímto způsobem mohou pomoci snížit náklady na zpracování poplatků kreditních karet. Maloobchodní prodejci proto mohou poskytnout slevy zákazníkům, kteří používají tyto alternativní typy úhrad.

V Microsoft Dynamics 365 Retail mohou maloobchodní prodejci konfigurovat procentuální slevu, která se použije na potvrzené řádky, pokud odběratel zaplatí použití preferovaného typu úhrady. Zákazník se může rozhodnout, zda provést částečnou platbu nebo celou platbu a zda bude v maloobchodu určena odpovídající částka slevy. Všimněte si, že sleva je vždy uvedena na základě částky před zdaněním opravňujících položek.

Slevy založené na úhradách nesoutěží s slevami založenými na položkách, jako jsou periodické nebo ruční slevy. Vždy jsou složeny ze slev položky. Proto i v případě, že je pro určitou položku použita exkluzivní časová sleva, bude sleva na základě úhrady stále uplatněna na výhradní časovou slevu. Obdobně, je-li pro transakci použita prahová sleva a sleva na základě úhrady snižuje celkový součet pod prahovou hodnotu, bude prahová sleva přesto uplatněna na transakci.

I když slevy založené na nabídkách snižují mezisoučet transakce, neovlivní automatické poplatky, které se vztahují na transakci. Jsou-li například náklady na dodání vypočteny jako $5, protože mezisoučet je vyšší než $100 a sleva na základě úhrady snižuje částku tak, aby byla nižší než $100, budou náklady na dodání dané objednávky stále $5.

> [!NOTE]
> Slevy založené na úhradách jsou proporcionálně distribuovány k opravňujícím řádkům prodeje a omezují částku předběžné daně jednotlivých řádků. Pokud je pro typ úhrady nakonfigurováno více slev na základě úhrady (například hotovost), použije se pouze nabízená sleva.

Slevy na základě úhrady lze použít pouze pro řádky prodeje, u kterých nejsou ceny uzamčeny. Pokud jsou do objednávky přidány nové řádky prodeje, bude sleva na základě úhrady použita na nové řádky prodeje pouze během platby. Při zaskladnění objednávky odběratele pro výdej nebo dodávku sleva na základě úhrady použije pouze na částku vkladu. Po dokončení objednávky budou v průběhu plnění zablokovány ceny prodejních řádků. Proto se žádná sleva na základě úhrady nepoužije pro žádný zůstatek, který je vyplacen během výdeje nebo autorizován během přepravy. Slevu na základě úhrady lze použít na celou částku objednávky odběratele pouze v případě, že maloobchodní prodejce při vystavení objednávky vypracuje celou částku jako zálohu.

> [!IMPORTANT]
> V maloobchodě jsou slevy na základě úhrady aktuálně omezeny na dva typy plateb: kreditní karty a hotovost.

## <a name="pos-user-experience"></a>Prostředí uživatele POS

Pokud je pro hotovost nastavena sleva založená na nabídce a pokladník na pokladním místě (POS) vybere tlačítko, které je mapováno na operaci platby v hotovosti, sleva na základě úhrady se automaticky použije pro transakci. Snížená částka se pak zobrazí jako zůstatek. Pokud však pokladník vybere tlačítko **Zpět** na obrazovce platby, sleva bude odstraněna a původní částka bude zobrazena na obrazovce transakce. Pokud je řádek platby anulován, dojde k odebrání slevy na základě úhrady.

U plateb kartou mohou maloobchodní prodejci nastavit slevu na základě úhrady jednoho nebo více typů kreditních karet. Systém však nemůže ověřit použitý typ kreditní karty, pokud není karta autorizována. Je-li sleva po autorizaci použita, autorizace platby bude mít vyšší částku, ale zachytávání plateb bude mít nižší částku.

Chcete-li předejít této situaci, zobrazí se v případě, kdy odběratel zaplatí kreditní kartou, pokladníkovi dialogové okno se seznamem kreditních karet, které zajistí další úspory pro zákazníka. Pokladník se pak může zeptat, zda chce zákazník použít jednu z preferovaných karet k získání dodatečné slevy. Pokud pokladník používá upřednostňovanou kartu, bude pro transakci použita sleva na základě úhrady a na obrazovce platby se zobrazí snížená částka. Autorizace bude pro sníženou částku. Pokud zákazník vloží kartu, která se liší od karty vybrané pokladníkem, zobrazí se chybová zpráva a autorizace je anulována.

## <a name="call-center-user-experience"></a>Uživatelské prostředí kontaktního střediska

Když uživatel vybere položku **Dokončeno** během objednávky kontaktního střediska, zobrazí se obrazovka **Součty**. Součty na této obrazovce nejprve nezahrnují slevy založené na úhradě, protože ještě nebyl vybrán způsob platby. Pokud uživatel na obrazovce **Přidat platbu** vybere způsob platby, pro který je nastavena sleva na základě úhrady, bude částka platby automaticky upravena tak, aby odpovídala zlevněné částce. Podobně jako zákazník v POS se může zákazník kontaktního centra rozhodnout, zda má zaplatit celou platbu nebo částečnou platbu. Na základě částky, která je zaplacena, bude sleva na základě úhrady použita pro prodejní objednávku.

> [!NOTE]
> Ověření karty pro objednávky kontaktních center není provedeno. Pokud například uživatel kontaktního centra vybere jako kreditní kartu Visa, ale zákazník používá funkci MasterCard, systém přesto použije slevu.

## <a name="exclude-items-from-discounts"></a>Vyloučení položek ze slev

Maloobchodní prodejci často vylučují některé produkty, jako jsou nové položky nebo položky na vyžádání, ze slev. Přesto však mohou chtít použít slevy založené na nabídkách. Maloobchodní prodejce například konfiguruje Maloobchod tak, aby nepovoloval slevy na základě položky nebo ruční slevy. Pokud však zákazník zaplatí používanou upřednostňovanou nabídkou, aplikace Maloobchod stále uplatňuje slevu založenou na nabídkách. Chcete-li aplikaci Maloobchod nastavit tímto způsobem, musí maloobchodní prodejci vypnout možnost **Zabránit všem slevám** a **Zabránit slevám založeným na úhradě** a zapnout možnost **Zabránit ručním slevám** a **Zabránit maloobchodním slevám**. Možnosti jsou na stránce **Vydané produkty** na kartě **Maloobchod**.

> [!NOTE]
> Pokud je zapnuta konfigurace **Zabránit všem slevám**, nebudou u produktu použity žádné slevy. Nebudou použity slevy na základě úhrad.
