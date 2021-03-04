---
title: Řešení problému s nákupními objednávkami
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s nákupními objednávkami.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424236"
---
# <a name="troubleshoot-purchase-orders"></a>Řešení problému s nákupními objednávkami

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s nákupními objednávkami.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Akce může být dokončena až po úplném distribuci čísla řádku.

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Když se nákupní objednávky importují prostřednictvím správy dat, čísla řádků nákupní objednávky nenásledují přírůstek definovaný v systémových parametrech.

### <a name="issue-description"></a>Popis problému

Ve výchozím nastavení automaticky generovaná čísla řádků pro řádky nákupní objednávky, které se importují prostřednictvím datové entity *Řádky nákupní objednávky V2* nepoužívají přírůstek čísla řádku systému, který je zadán v systémových parametrech. Pokud ručně vytvoříte nákupní objednávku a přidáte řádky prostřednictvím uživatelského rozhraní, budou čísla řádků správně zvýšena. Pokud však používáte Data management framework (DMF), nejsou správně zvýšena.

K tomuto problému dochází, protože při importu řádků pomocí DMF, pokud čísla řádků již nejsou přiřazena v importované entitě, systém používá k jejich přiřazení metodu DMF. Tato metoda vždy zvyšuje čísla řádků o jedno.

### <a name="issue-workaround"></a>Řešení problému

Ujistěte se, že požadovaná čísla řádků jsou již uvedena v polích čísel řádků datové entity při importu řádků nákupní objednávky. V tomto případě DMF nepřepíše čísla řádků.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Z účtu faktury není vyplněna výchozí daňová skupina a výchozí platební sleva.

Pokud používáte účet faktury, který se liší od účtu zákazníka, nevyplní se při vytvoření nákupní objednávky výchozí daňová skupina a výchozí platební sleva z účtu faktury.

Toto chování je záměrné. Výchozí hodnoty pro daňovou skupinu, platební slevy a další informace o cenách jsou založeny na účtu zákazníka, nikoli na účtu faktury.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Během potvrzení nákupní objednávky se mi zobrazí chyba „Odkaz na objekt není nastaven“ nebo během zaúčtování faktury dodavatele dojde k výjimce „Byla vyvolána výjimka cílem vyvolání“.

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.

### <a name="issue-description"></a>Popis problému

Zobrazí se následující chyba: „Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.“

### <a name="issue-resolution"></a>Řešení problému

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Mohu zobrazit pouze nákupní objednávky, které jsem vytvořil/a?

Tato funkce není aktuálně k dispozici.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Mohu rezervovat zásoby a vytvořit transakce proti registrovaným zásobám na nákupní objednávce?

### <a name="issue-description"></a>Popis problému

I když jsou položky ve stavu *Registrováno* na nákupní objednávce, zásoby si stále můžete rezervovat. Jinými slovy můžete vytvářet transakce proti registrovaným zásobám.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Vytvoření nákupní objednávky.
2. Zaregistrujte řádek nákupní objednávky.
3. Všimněte si, že můžete generovat rezervace nebo transakce proti registrovaným zásobám.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Očekává se, že registrované položky fyzicky dorazily do skladu nebo zásob a že jsou proto k dispozici k rezervaci.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Nákupní objednávky neodrážejí jazykové nastavení právnické osoby.

### <a name="issue-description"></a>Popis problému

Název produktu na nákupní objednávce se zobrazuje v jazyce systému místo v jazyce nastaveném pro právnickou osobu, kde byla vytvořena nákupní objednávka.

### <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Nastavte jazyk systému na *EN-US* (americká angličtina).
1. Ujistěte se, že existuje produkt, kde jsou udržovány jazyky *EN-US* a *DE* (němčina) pro překlady názvu produktu.
1. Změňte jazyk právnické osoby na *DE*.
1. V právnické osobě, kde je jako jazyk nastaveno *DE*, vytvořte nákupní objednávku, která zahrnuje produkt.
1. Všimněte si, že název produktu je stále zobrazen v americké angličtině (systémový jazyk).

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Na nákupních objednávkách je produkt vždy zobrazen v systémovém jazyce. Při vytvoření deníku potvrzení se použije jazyk nákupní objednávky.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Seznam schválených dodavatelů podle entity produktu neumožňuje změnu data účinnosti.

### <a name="issue-description"></a>Popis problému

Produkt má schváleného dodavatele, který má například datum účinnosti 11. ledna 2018 (*01/11/2018*) a datum vypršení platnosti *Nikdy*. Pokud se pokusíte změnit datum účinnosti na 10. ledna 2018 (*01/10/2018*) nebo 12. ledna 2018 (*01/12/2018*), zobrazí se následující chyba:

> Nelze vytvořit záznam v seznamu schválených dodavatelů (PdsApproveVendorList). Hodnota „Vypršení platnosti“ musí být větší nebo rovna hodnotě „Datum platnosti“.

### <a name="issue-resolution"></a>Řešení problému

Můžete prodloužit pouze období, pro které je dodavatel schválen. Platí následující pravidla:

- Chcete-li změnit datum účinnosti tak, aby bylo dřívější než kterýkoli z existujících záznamů (období) pro dodavatele položky, datum vypršení platnosti nového období musí být před všemi daty vypršení platnosti v existujících záznamech.
- Chcete-li změnit datum vypršení platnosti tak, aby bylo pozdější než kterékoli z existujících období, datum platnosti musí být po posledním datu vypršení platnosti v jakémkoli existujícím záznamu.
- Chcete-li snížit celkovou dobu, po kterou je dodavatel schválen, musíte odstranit nebo upravit existující záznamy. Případně můžete použít přepínač **zkrátit** během importu. Tento přepínač odstraní všechny existující záznamy v tabulce pro schválené dodavatele podle položek.

Pro příklad scénáře, který je popsán v popisu problému, kde má záznam datum účinnosti *01/11/2018* a datum vypršení platnosti *Nikdy*, můžete importovat nový záznam, který má datum účinnosti *01/10/2018* a datum vypršení platnosti *Nikdy*. Nelze však zkrátit období tak, aby bylo datum účinnosti aktualizováno na *01/12/2018* prostřednictvím správy dat. Tuto změnu musíte provést prostřednictvím uživatelského rozhraní.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Po změně dodací adresy v záhlaví nákupní objednávky se název dodávky nesynchronizuje.

### <a name="issue-description"></a>Popis problému

Adresa v záhlaví nákupní objednávky se aktualizuje na adresu, která není doručovací adresou. I když je adresa na nákupní objednávce aktualizována, název dodávky není aktualizován na základě aktualizované adresy.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. Vybraná adresa musí být klasifikována jako doručovací adresa. Jinak se název doručení neaktualizuje na základě vybrané adresy.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Mohu najít uživatele, který zrušil nákupní objednávku?

Tyto informace jsou sledovány pouze v případě, že je u objednávky možné provádět změny. Pokud používáte správu změn, můžete vidět, kdo změnu (zrušení) odeslal a kdo ji schválil.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]