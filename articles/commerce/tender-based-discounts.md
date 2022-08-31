---
title: Slevy založené na úhradě
description: Tento článek popisuje funkci slevy na základě úhrady, které prodejcům umožňují konfigurovat specifické typy úhrad v Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: 3c28297e62e5b2880a7a39381702d5a1448c91ac
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336647"
---
# <a name="tender-based-discount"></a>Sleva založená na úhradě

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tento článek popisuje funkci slevy na základě úhrady, které prodejcům umožňují konfigurovat specifické typy úhrad v Microsoft Dynamics 365 Commerce.

Jedná se o běžný postup v rámci maloobchodních prodejců při uvolňování soukromých kreditních karet. Maloobchodní prodejci z toho mají prospěch, protože získají upřednostňované sazby od bank. Vzhledem k tomu, že tyto kreditní karty mohou zákazníky povzbudit k častějším návštěvám obchodu, pomáhají zlepšit hlavní řádek maloobchodníka. Maloobchodníci proto mají motivaci ke zvýšení zákaznických kreditních karet. Když chtějí dosáhnout tohoto cíle, často poskytují zákazníkům, kteří tyto kreditní karty používají, další slevy.

Maloobchodníci, kteří neposkytují kreditní karty, mohou například případně požadovat, aby zákazníci zaplatili pomocí jiných typů úhrad, jako jsou hotovost, dárkové poukazy nebo věrnostní body. Tímto způsobem mohou pomoci snížit náklady na zpracování poplatků kreditních karet. Maloobchodní prodejci proto mohou poskytnout slevy zákazníkům, kteří používají tyto alternativní typy úhrad.

## <a name="tender-based-discount"></a>Sleva založená na úhradě

Commerce podporuje *slevu založenou na úhradě*, která maloobchodníkům umožňuje nakonfigurovat procento slevy, které se použije na transakci, pokud celková částka transakce přesáhne určitou částku a zákazník zaplatí pomocí preferovaného typu platby. Sleva založená na úhradě je založena na úrovních, takže různé procenta slevy mohou být spojeny s různými prahovými hodnotami částky. Zákazník se může rozhodnout, zda provést částečnou platbu nebo celou platbu a cenový modul určuje odpovídající částku slevy. Sleva na základě úhrady je vždy uvedena na částce prodejních řádků před zdaněním.

Slevu založeou na úhradě lze použít pouze na řádky prodeje, kde není cena uzamčena, a sleva je proporčně rozdělena mezi kvalifikované řádky. Pokud jsou do objednávky přidány nové řádky prodeje, bude sleva na základě úhrady použita na nové řádky prodeje pouze během platby. Při zaskladnění objednávky odběratele pro výdej nebo doručení se sleva na základě úhrady použije pouze na částku vkladu. Po dokončení objednávky budou v průběhu plnění zablokovány ceny prodejních řádků. Žádná sleva na základě úhrady se nepoužije pro žádný zůstatek, který je vyplacen během výdeje nebo autorizován během přepravy. Slevu na základě úhrady lze použít na celou částku objednávky odběratele pouze v případě, že maloobchodní prodejce při vystavení objednávky vypracuje celou částku jako zálohu.

Slevy na základě úhrady nekonkurují slevám na základě položek, jako jsou jednoduché slevy, množstevní slevy, mezní slevy, kombinační slevy a manuální slevy. Slevy na základě úhrady se vždy sčítají se slevami na základě položky. Proto i v případě, že je pro určitou položku použita exkluzivní sleva, bude sleva na základě úhrady stále uplatněna na výhradní slevu. Obdobně, je-li pro transakci použita prahová sleva a sleva na základě úhrady snižuje celkový součet pod prahovou hodnotu, bude prahová sleva přesto uplatněna na transakci.

I když slevy založené na nabídkách snižují mezisoučet transakce, neovlivní automatické poplatky, které se vztahují na transakci. Jsou-li například náklady na dodání vypočteny jako $5, protože mezisoučet je vyšší než $100 a sleva na základě úhrady snižuje částku tak, aby byla nižší než $100, budou náklady na dodání dané objednávky stále $5.

Sleva na základě úhrady je aktuálně omezena na dva typy plateb: kreditní karty a hotovost. Pokud je pro typ platby nakonfigurováno více slev na základě úhrady, použije se pouze nabízená sleva.

## <a name="pos-user-experience"></a>Prostředí uživatele POS

Pokud je pro hotovost nastavena sleva založená na úhradě a pokladník na pokladním místě (POS) vybere tlačítko **Platba v hotovosti** pro kontrolu transakce cash and carry, které je mapováno na operaci platby v hotovosti, sleva na základě úhrady se automaticky použije pro transakci. Snížená částka se pak zobrazí jako zůstatek. Pokud však pokladník vybere tlačítko **Zpět** na obrazovce platby, sleva bude odstraněna a původní částka bude zobrazena na obrazovce transakce. Pokud je řádek platby anulován, dojde k odebrání slevy na základě úhrady.

U plateb platební kartou mohou maloobchodní prodejci nastavit slevu na základě úhrady jednoho nebo více typů kreditních karet. Systém však nemůže ověřit použitý typ kreditní karty, pokud není karta autorizována. Je-li sleva po autorizaci použita, autorizace platby bude mít vyšší částku, ale zachytávání plateb bude mít nižší částku. Chcete-li předejít této situaci, zobrazí se v případě, kdy odběratel zaplatí kreditní kartou, pokladníkovi dialogové okno se seznamem preferovaných kreditních karet, které zajistí další slevu pro zákazníka. Pokladník se pak může zeptat, zda chce zákazník použít jednu z preferovaných karet k získání dodatečné slevy. Pokud pokladník vybere upřednostňovanou kartu, bude pro transakci použita sleva na základě úhrady a na obrazovce platby se zobrazí snížená částka. Autorizace bude pro sníženou částku. Pokud zákazník vloží kartu, která se liší od karty vybrané pokladníkem, zobrazí se chybová zpráva a autorizace je anulována.

## <a name="call-center-user-experience"></a>Uživatelské prostředí kontaktního střediska

Když uživatel call centra vybere položku **Dokončeno** během objednávky kontaktního střediska, zobrazí se obrazovka **Součty**. Součty na této obrazovce nejprve nezahrnují slevy založené na úhradě, protože ještě nebyl vybrán způsob platby. Pokud uživatel na obrazovce **Přidat platbu** vybere způsob platby, pro který je nastavena sleva na základě úhrady, bude částka platby automaticky upravena tak, aby odpovídala zlevněné částce. Podobně jako zákazník v POS se může zákazník kontaktního centra rozhodnout, zda má zaplatit celou platbu nebo částečnou platbu. Na základě částky, která je zaplacena, bude sleva na základě úhrady použita pro prodejní objednávku.

> [!NOTE]
> Ověření karty pro objednávky kontaktních center není provedeno. Pokud například uživatel kontaktního centra vybere jako kreditní kartu Visa, ale zákazník používá funkci MasterCard, systém přesto použije slevu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
