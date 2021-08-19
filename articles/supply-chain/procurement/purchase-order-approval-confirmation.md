---
title: Schválení a potvrzení nákupních objednávek
description: Toto téma popisuje stavy, kterými prochází nákupní objednávka poté, co byla vytvořena, a efekt umožňující správu změn v nákupních objednávkách.
author: kamaybac
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580095bacafe74c9e22aba47ca657e1cf42b3c6ae7929478a0d2f8bd241868f1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780119"
---
# <a name="approve-and-confirm-purchase-orders"></a>Schválení a potvrzení nákupních objednávek

[!include [banner](../includes/banner.md)]

Toto téma popisuje stavy, kterými prochází nákupní objednávka poté, co byla vytvořena, a efekt umožňující správu změn v nákupních objednávkách.

Po vytvoření by měla nákupní objednávka projít schvalovacím procesem. Jakmile dodavatel odsouhlasí s objednávku, nákupní objednávka bude nastavena na stav **Potvrzeno**.

## <a name="approval-of-purchase-orders"></a>Schválení nákupních objednávek
Nákupní objednávky, které nepoužívají správu změn, mají stav **Schváleno** ihned po jejich vytvoření, zatímco nákupní objednávky, které používají správu změn, jsou po vytvoření ve stavu **Návrh**. Nákupní objednávka, která byla vytvořena při potvrzení plánované objednávky z hlavního plánování, je vždy nastavena na stav **Schváleno** bez ohledu na nastavení správy změn. Nákupní objednávka vytváří skladové transakce pouze v případě, že dosáhne stavu **Schváleno**. Proto se dané zásoby nezobrazují jako dostupné pro rezervaci nebo označení, dokud objednávka nebude přijata.

Správu změn pro nákupní objednávky povolíte nastavením možnosti **Aktivovat správu změn** na stránce **Parametry modulu Zásobování a zdroje**. Pokud je povolena správa změn, nákupní objednávky musí po dokončení projít workflowem schválení. Aplikace Supply Chain Management má editor procesu workflowu, kde můžete definovat workflow představující proces schválení. Tento pracovní postup může zahrnovat pravidla pro automatické schválení, pravidla, která určují, kdo bude přiřazen ke schválení konkrétních nákupních objednávek, a pravidla pro předání pracovního postupu, který čekal dlouhou dobu na schválení. Můžete povolit proces řízení změn pro všechny dodavatele nebo jen pro konkrétní dodavatele. Proces lze také nastavit tak, aby jej bylo možné přepsat pro jednotlivé nákupní objednávky.

Pokud je povolena správa změn, nákupní objednávky prochází šesti stavy schválení od **Návrh** po **Dokončeno**. Po schválení objednávky musí uživatelé, kteří ji chtějí změnit, použít akci **Požadavek na změnu**.

| Stav schválení | Popis                                                                      | Požadavek na změnu je povolen. |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Koncept           | Nákupní objednávka je ve stavu Návrh a nebyla odeslána ke schválení v pracovním postupu nákupní objednávky.     | Ne                        |
| Probíhá kontrola       | Nákupní objednávka byla předložena ke schválení v pracovním postupu nákupní objednávky. Čeká se na schválení.       | Č.                        |
| Odmítnuto        | Nákupní objednávka byla odmítnuta během procesu schvalování.                                 | Č.                        |
| Schváleno        | Nákupní objednávka byla schválena.                                                             | Ano                       |
| Potvrzeno       | Nákupní objednávka byla potvrzena. Nákupní objednávky nelze potvrdit, dokud nedojde k jejich schválení.        | Ano                       |
| Finalizováno       | Nákupní objednávka byla dokončena. Nyní je finančně uzavřena a nemůže již být změněna. | Ne                        |

## <a name="confirming-purchase-orders"></a>Potvrzení nákupních objednávek
Nákupní objednávky, které mají stav schválení **Schváleno**, mohou projít dalšími kroky před jejich potvrzením. Například může být nutné odeslat dotaz na nákup dodavateli s dotazem na cenu, slevy nebo data dodání. V takovém případě můžete nastavit nákupní objednávku na stav **Na externí kontrole** pomocí akce **Nákupní dotaz**.

Dodavatelé, kteří jsou nastaveni pro použití portálu pro dodavatele, mohou kontrolovat objednávky z portálu, a zde je také schválit nebo zamítnout. Během tohoto procesu kontroly mají nákupní objednávky stav **Na externí kontrole**. Je možné nakonfigurovat portál pro dodavatele tak, aby potvrzení od dodavatele automaticky potvrdilo objednávku v aplikaci Supply Chain Management. Případně můžete ručně ověřit nákupní objednávku po obdržení potvrzení od dodavatele. Jestliže dodavatel odmítne nákupní objednávku, odmítnutí je přijato společně s důvodem zamítnutí a návrhy na změny. V tomto případě zůstává stav nákupní objednávky **Na externí kontrole**.

Existuje také možnost vygenerovat proforma potvrzení pro objednávku ještě před skutečným zpracováním potvrzení. Tato volba vytvoří jednoduše sestavu, kterou můžete sdílet s dodavatelem. Nevytváří žádné informace v deníku.

Poté, co dodavatel souhlasil s objednávkou, je dalším krokem označení nákupní objednávky jako potvrzené. Dokončení tohoto kroku je možné buď pomocí akce **Potvrzení** nebo **Potvrdit**. Obě tyto akce nastaví stav schválení objednávky na **Potvrzeno**. Potvrzení objednávky iniciuje další dva procesy:

-   Je vytvořen deník pro uložení přesné kopie toho, co bylo potvrzeno v systému. V některých případech vyžadují objednávky změny, a další deníky jsou vytvořeny po potvrzení aktualizované objednávky. Tyto deníky umožňují zobrazit historii různých verzí objednávky, které byly potvrzeny.
-   Jsou vytvořena rozúčtování a v případě povolení příslušné funkce proběhne kontrola objednávky a kontrola rozpočtu. Pokud kontrola selže, zobrazí se chybová zpráva oznamující, že je nutno provést změny, než bude možné nákupní objednávku znovu potvrdit.

Dodavatel může požádat o nějaký typ záruky toho, že bude odeslána platba za nákup. Existují různé metody poskytnutí této záruky v rámci zpracování závazků. Například akce **Záloha** si vyhradí finanční prostředky pro nákupní objednávku, a tato záloha je zaznamenána v nákupní objednávce.

## <a name="changing-purchase-orders"></a>Změna nákupních objednávek
V některých případech může být nutné změnit nákupní objednávku poté, co dosáhne stavu schválení **Schváleno** nebo **Potvrzeno**.

Pokud byla nákupní objednávka vytvořena pomocí procesu řízení změn, můžete provádět změny vyvoláním objednávky, nebo pokud objednávka již byla schválena, tak pomocí akce **Požadavek na změnu**. V takovém případě je stav schválení upraven zpět na **Návrh**, a vy pak můžete změnit pořadí. Po provedení změn bude pravděpodobně nutné předložit nákupní objednávku k opětovnému schválení. Můžete nakonfigurovat typy změn, které vyžadují opětovné schválení, pomocí pravidla zásad **Pravidlo opětovného schválení pro nákupní objednávky** na stránce **Zásady nákupu**.

Pokud byla dodána část objednaného množství pro řádek nákupní objednávky, nelze již objednané množství změnit, když je nákupní objednávka ve stavu **Koncept**. Můžete však změnit množství **zbývající dodávky** na řádku pro nákupní objednávku ve stavu **koncept**.

Jakmile je objednávka potvrzena, nemůžete ji již odstranit. Můžete však zrušit celkové množství nebo libovolné zbývající množství na objednávce, a to za předpokladu, že množství nebylo přijato nebo fakturováno. Poté můžete použít akci **Dokončit** k zabránění dalšímu zpracování. 


## <a name="canceling-purchase-orders"></a>Zrušení nákupních objednávek

Nákupní objednávku lze zrušit pomocí akce **Storno** v záhlaví.

Pokud bylo množství částečně registrováno, přijato nebo fakturováno, můžete zrušit pouze zbývající množství, které nebylo zaregistrováno, přijato nebo fakturováno. Objednané množství se pak sníží odpovídajícím způsobem. Po aktualizaci množství na řádku se také aktualizuje stav řádku. Původní množství na řádku je například 5 a je přijato množství 3. V takovém případě lze zrušit pouze dvě. Řádek bude poté aktualizován na stav **Přijato**.

Pokud je do řádku objednávky přidán zůstatek k dodání, který překračuje množství na řádku objednávky, akce **stornování** neodstraní nadbytečné množství. Místo toho zůstane řádek ve stavu **Otevřená objednávka**, protože má zbývající množství. Původní množství na řádku je například 5 a zbývající část dodávky je 7. Pokud je objednávka zrušena, pět se zruší a množství 2 zůstane, jak lze zobrazit ve skladových transakcích.

Chcete-li zrušit celé množství na řádku NO, zrušte v řádku zbývající množství dodání. Řádek bude poté aktualizován na stav **Zrušeno**.

Pokud PO prochází správou změn, každá změna, například zrušení objednávky nebo zůstatek dodávky, musí být před dokončením procesu odeslána do systému workflowu a schválena a skladové transakce mohou být aktualizovány jako zrušené.

## <a name="additional-resources"></a>Další zdroje

[Přehled nákupních objednávek](purchase-order-overview.md)

[Vytváření nákupních objednávek](purchase-order-creation.md)

[Příjemka produktu proti nákupním objednávkám](product-receipt-against-purchase-orders.md)

[Přehled faktur dodavatele](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]