---
title: Řešení problémů s cenami, slevami, smlouvami a rabaty
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s cenami, slevami, smlouvami a rabaty.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 237ec60823eb5fded09c32d6a51b1eb504456a1dc666d7d6f2e6678382433de9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762835"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Řešení problémů s cenami, slevami, smlouvami a rabaty

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s cenami, slevami, smlouvami a rabaty.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Po vytvoření nákupní objednávky nemohu propojit nákupní smlouvu s řádkem nákupní objednávky.

Po vytvoření nákupní objednávky musí být k nákupní objednávce přiřazena nákupní smlouva. Jinak nelze řádky nákupní objednávky přidružit k řádkům kupní smlouvy.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Jaká kontrola spustí zprávu „Aktualizovat ceny a slevy zadané ručně nebo externí dokument“?

Když změníte datum odeslání, může se zobrazit zpráva „Aktualizovat ceny a slevy zadané ručně nebo externí dokument.“ Tuto zprávu obdržíte proto, že když se změní datum odeslání, může být spuštěna jiná obchodní nebo prodejní smlouva a způsobit změnu ceny. Změna data odeslání může také ovlivnit plány skladu a další související informace.

Zpráva se spustí vždy, když dojde ke změně některého z dat nebo některých dalších parametrů. Účelem zprávy je ujistit se, že jste si vědomi cenových změn, které mohou na základě těchto změn nastat.

Zpráva je výzvou k vyhodnocení obchodní smlouvy. Celý popis najdete v tématu [Zásady hodnocení obchodní smlouvy](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Příjemka nákupní objednávky nezahrnuje všechny poplatky.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Na stránce **Parametry modulu Zásobování a zdroje** na kartě **Dodávka** se ujistěte, že možnost **Generovat náklady na příjemce produktu** je nastavena na *Ano*.
1. Vytvořte nákupní objednávku, která obsahuje náklady.
1. Potvrďte nákupní objednávku.
1. Přijměte nákupní objednávku.
1. Podívejte se na celkový příjem a porovnejte jej s očekávaným součtem.
1. Všimněte si, že ne všechny poplatky jsou zahrnuty v příjemce nákupní objednávky.

### <a name="issue-resolution"></a>Řešení problému

Řešení závisí na způsobu, jakým byly nastaveny vedlejší náklady. Informace o tom, jak nastavit vedlejší náklady podle vašich požadavků, najdete v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Ceny a slevy z obchodních smluv se neuplatňují na řádcích prodejních nebo nákupních objednávek, které se importují prostřednictvím správy dat.

### <a name="issue-description"></a>Popis problému

Obchodní smlouvy, které se vztahují na řádky prodejních nebo nákupních objednávek, se neuplatňují na řádky, které se importují prostřednictvím správy dat. Stejné obchodní smlouvy se však používají na řádcích prodejních nebo nákupních objednávek, které se vytvářejí ručně.

### <a name="reason-for-the-issue"></a>Důvod problému

Pokud řádky nákupní objednávky, které jsou importovány prostřednictvím správy dat, již obsahují informace o ceně, obchodní smlouva nebude u těchto řádků přehodnocena. Například pokud **Procento slevy řádku** nebo některá z cenových a slevových hodnot je pro řádek nastaveno , pak nebudou obchodní smlouvy pro daný řádek vyhledávány.

### <a name="issue-workaround"></a>Řešení problému

Toto chování se očekává a je podobné pro prodejní i nákupní objednávky.

Řešením je importovat řádky nákupní objednávky bez nastavení jakýchkoli informací o ceně. Poté budou použity obchodní smlouvy a řádky nákupní objednávky budou aktualizovány na základě definovaných obchodních smluv.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Rabat dodavatele se nesčítá na základě faktur.

### <a name="issue-description"></a>Popis problému

Pokud zaúčtované faktury mají různá data splatnosti, tyto faktury se neprojeví v rabatech dodavatelů, které se z nich generují.

### <a name="issue-resolution"></a>Řešení problému

Datum splatnosti se při výpočtu rabatu dodavatele úmyslně nezohledňuje. Zvažte přizpůsobení systému tak, aby datum splatnosti a vztah k faktuře byly zjevnější s ohledem na skutečný rabat dodavatele.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Jednotkové ceny u nákupních objednávek se nevypočítávají na základě převodu jednotek.

### <a name="issue-description"></a>Popis problému

Když se na nákupní objednávce změní jednotka, ceny obchodních smluv se nepřepočítají podle definic převodu jednotek.

### <a name="issue-resolution"></a>Řešení problému

Ceny se vždy získávají z obchodních smluv (nebo jiného nastavení cen v systému, jako jsou prodejní smlouvy nebo ceny zboží), a jsou stanoveny pro jednotku.

Pokud je jednotka změněna na řádku objednávky, systém vyhledá cenu pro novou jednotku a použije tuto cenu. Pokud pro jednotku není nalezena žádná cena, systém cenu nepoužije. Převod jednotky nelze použít k přepočtu ceny na jinou jednotku. Teoreticky se cena za jednu krabici z deseti nemusí rovnat desetinásobku ceny jedné krabice.

### <a name="issue-workaround"></a>Řešení problému

Jedním ze způsobů, jak tento problém vyřešit, je zajistit, aby existovaly obchodní smlouvy pro jednotky, u kterých očekáváte, že budou použity na řádcích objednávek pro položku.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>U obchodních smluv dochází k problémům s převodem měn.

Ceny obchodních smluv se nepřepočítají podle měny, když se měna liší od nákupní objednávky.

Funkce *Obecná měna* umožňuje definovat ceny a slevy pouze v jedné měně. Poté můžete převádět na jiné měny podle potřeby. Po dokončení převodu může funkce navíc automaticky použít inteligentní zaokrouhlování.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Když otevřu stránku Nákupní smlouva v režimu zobrazení řádku, nemohu stránku přizpůsobit přidáním pole Cena jednotky v přehledu řádku.

Některá sdílená pole v rámci smlouvy nelze zahrnout do přizpůsobení. K tomuto omezení dochází z důvodu implementovaného datového modelu. Proto nemůžete přizpůsobit pole **Jednotka ceny**.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Maximální limit z nákupní smlouvy není účinný u nákupní žádanky.

### <a name="issue-description"></a>Popis problému

Pokud je nákupní žádanka propojena s nákupní smlouvou, maximální limit z nákupní smlouvy neplatí na nákupní žádance. Informace o výchozí ceně jsou správně zadány, ale v nákupní žádance lze objednat více, než je maximální limit z kupní smlouvy.

### <a name="issue-resolution"></a>Řešení problému

Toto chování se očekává. Protože žádanky nejsou vždy schváleny, nemělo by být v nákupní smlouvě vyhrazeno množství nebo částka. Proto nesplníte maximální limit z nákupní smlouvy.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Obchodní smlouvy lze uzavřít z odmítnutých požadavků na cenovou nabídku. Systém tedy nebrání vytváření deníků obchodních smluv, pokud nebyl přijat řádek RFQ.

Můžete vytvořit obchodní smlouvy pro jakékoli odpovědi na požadavky na nabídku (RFQ), bez ohledu na to, zda byly přijaty nebo odmítnuty. Další informace naleznete v tématu [Přehled požadavků na nabídku](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]