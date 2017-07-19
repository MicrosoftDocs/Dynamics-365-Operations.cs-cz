---
title: "Schválení a potvrzení nákupních objednávek"
description: "Tento článek popisuje stavy, kterými prochází nákupní objednávka poté, co byla vytvořena, a efekt umožňující správu změn v nákupních objednávkách."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0ec91bcf0ab334585eefae2fe54750c45419682e
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="approve-and-confirm-purchase-orders"></a>Schválení a potvrzení nákupních objednávek

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Tento článek popisuje stavy, kterými prochází nákupní objednávka poté, co byla vytvořena, a efekt umožňující správu změn v nákupních objednávkách.

Po vytvoření by měla nákupní objednávka projít schvalovacím procesem. Jakmile dodavatel odsouhlasí s objednávku, nákupní objednávka bude nastavena na stav **Potvrzeno**.

## <a name="approval-of-purchase-orders"></a>Schválení nákupních objednávek
Nákupní objednávky, které nepoužívají správu změn, mají stav **Schváleno** ihned po jejich vytvoření, zatímco nákupní objednávky, které používají správu změn, jsou po vytvoření ve stavu **Návrh**. Nákupní objednávka, která byla vytvořena při potvrzení plánované objednávky z hlavního plánování, je vždy nastavena na stav **Schváleno** bez ohledu na nastavení správy změn. Nákupní objednávka vytváří skladové transakce pouze v případě, že dosáhne stavu **Schváleno**. Proto se dané zásoby nezobrazují jako dostupné pro rezervaci nebo označení, dokud objednávka nebude přijata.  

Správu změn pro nákupní objednávky povolíte nastavením možnosti **Aktivovat správu změn** na stránce **Parametry modulu Zásobování a zdroje**. Pokud je povolena správa změn, nákupní objednávky musí po dokončení projít workflowem schválení. Aplikace Microsoft Dynamics 365 for Finance and Operations má editor procesu workflowu, kde můžete definovat workflow představující proces schválení. Tento pracovní postup může zahrnovat pravidla pro automatické schválení, pravidla, která určují, kdo bude přiřazen ke schválení konkrétních nákupních objednávek, a pravidla pro předání pracovního postupu, který čekal dlouhou dobu na schválení. Můžete povolit proces řízení změn pro všechny dodavatele nebo jen pro konkrétní dodavatele. Proces lze také nastavit tak, aby jej bylo možné přepsat pro jednotlivé nákupní objednávky.  

Pokud je povolena správa změn, nákupní objednávky prochází šesti stavy schválení od **Návrh** po **Dokončeno**. Po schválení objednávky musí uživatelé, kteří ji chtějí změnit, použít akci **Požadavek na změnu**.

| Stav schválení | Popis                                                                      | Požadavek na změnu je povolen |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Koncept           | Nákupní objednávka je ve stavu Návrh a nebyla odeslána ke schválení v pracovním postupu nákupní objednávky.     | Č.                        |
| Probíhá kontrola       | Nákupní objednávka byla předložena ke schválení v pracovním postupu nákupní objednávky. Čeká se na schválení.       | Č.                        |
| Odmítnuto        | Nákupní objednávka byla odmítnuta během procesu schvalování.                                 | Č.                        |
| Schváleno        | Nákupní objednávka byla schválena.                                                             | Ano                       |
| Potvrzeno       | Nákupní objednávka byla potvrzena. Nákupní objednávky nelze potvrdit, dokud nedojde k jejich schválení.        | Ano                       |
| Dokončeno       | Nákupní objednávka byla dokončena. Nyní je finančně uzavřena a nemůže již být změněna. | Č.                        |

## <a name="confirming-purchase-orders"></a>Potvrzení nákupních objednávek
Nákupní objednávky, které mají stav schválení **Schváleno**, mohou projít dalšími kroky před jejich potvrzením. Například může být nutné odeslat dotaz na nákup dodavateli s dotazem na cenu, slevy nebo data dodání. V takovém případě můžete nastavit nákupní objednávku na stav **Na externí kontrole** pomocí akce **Nákupní dotaz**.  

Dodavatelé, kteří jsou nastaveni pro použití portálu pro dodavatele, mohou kontrolovat objednávky z portálu, a zde je také schválit nebo zamítnout. Během tohoto procesu kontroly mají nákupní objednávky stav **Na externí kontrole**. Je možné nakonfigurovat portál pro dodavatele tak, aby potvrzení od dodavatele automaticky potvrdilo objednávku v aplikaci Finance and Operations. Případně můžete ručně ověřit nákupní objednávku po obdržení potvrzení od dodavatele. Jestliže dodavatel odmítne nákupní objednávku, odmítnutí je přijato společně s důvodem zamítnutí a návrhy na změny. V tomto případě zůstává stav nákupní objednávky **Na externí kontrole**.  

Existuje také možnost vygenerovat proforma potvrzení pro objednávku ještě před skutečným zpracováním potvrzení. Tato volba vytvoří jednoduše sestavu, kterou můžete sdílet s dodavatelem. Nevytváří žádné informace v deníku.  

Poté, co dodavatel souhlasil s objednávkou, je dalším krokem označení nákupní objednávky jako potvrzené. Dokončení tohoto kroku je možné buď pomocí akce **Potvrzení** nebo **Potvrdit**. Obě tyto akce nastaví stav schválení objednávky na **Potvrzeno**. Potvrzení objednávky iniciuje další dva procesy:

-   Je vytvořen deník pro uložení přesné kopie toho, co bylo potvrzeno v systému. V některých případech vyžadují objednávky změny, a další deníky jsou vytvořeny po potvrzení aktualizované objednávky. Tyto deníky umožňují zobrazit historii různých verzí objednávky, které byly potvrzeny.
-   Jsou vytvořena rozúčtování a v případě povolení příslušné funkce proběhne kontrola objednávky a kontrola rozpočtu. Pokud kontrola selže, zobrazí se chybová zpráva oznamující, že je nutno provést změny, než bude možné nákupní objednávku znovu potvrdit.

Dodavatel může požádat o nějaký typ záruky toho, že bude odeslána platba za nákup. Existují různé metody poskytnutí této záruky v rámci zpracování závazků. Například akce **Záloha** si vyhradí finanční prostředky pro nákupní objednávku, a tato záloha je zaznamenána v nákupní objednávce.

## <a name="changing-purchase-orders"></a>Změna nákupních objednávek
V některých případech může být nutné změnit nákupní objednávku poté, co dosáhne stavu schválení **Schváleno** nebo **Potvrzeno**.  

Pokud byla nákupní objednávka vytvořena pomocí procesu řízení změn, můžete provádět změny vyvoláním objednávky, nebo pokud objednávka již byla schválena, tak pomocí akce **Požadavek na změnu**. V takovém případě je stav schválení upraven zpět na **Návrh**, a vy pak můžete změnit pořadí. Po provedení změn bude pravděpodobně nutné předložit nákupní objednávku k opětovnému schválení. Můžete nakonfigurovat typy změn, které vyžadují opětovné schválení, pomocí pravidla zásad **Pravidlo opětovného schválení pro nákupní objednávky** na stránce **Zásady nákupu**.  

Pokud byla dodána část objednaného množství pro řádek nákupní objednávky, nelze již objednané množství změnit. Můžete však změnit množství **Zbývá dodat** na řádku. Poté můžete použít akci **Dokončit** ke zrušení řádků a zabránění dalšímu zpracování. 

Jakmile je objednávka potvrzena, nemůžete ji již odstranit. Můžete však zrušit celkové množství nebo libovolné zbývající množství na objednávce, a to za předpokladu, že množství nebylo přijato nebo fakturováno.

<a name="see-also"></a>Viz také
--------

[Přehled nákupních objednávek](purchase-order-overview.md)

[Vytvoření nákupní objednávky](purchase-order-creation.md)

[Příjem produktů proti nákupním objednávkám](product-receipt-against-purchase-orders.md)

[Přehled faktur dodavatele](/dynamics365/unified-operations/financials/accounts-payable/vendor-invoices-overview)




