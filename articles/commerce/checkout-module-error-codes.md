---
title: Referenční kódy chyb modulu pokladny
description: Tento článek popisuje referenční kódy chyb pokladního modulu, které se zobrazují v chybových zprávách pro uživatele v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709653"
---
# <a name="checkout-module-error-reference-codes"></a>Referenční kódy chyb modulu pokladny

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tento článek popisuje kódy chyb pokladního modulu, které se zobrazují v chybových zprávách pro uživatele v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce zavedlo standardizované odkazy na chyby, které lze zahrnout do chyb pokladny online kanálu, které jsou prezentovány online zákazníkům. Ve verzi Commerce 10.0.31 a novější obsahují chybové zprávy v modulu pokladny chybové kódy a nezobrazují online zákazníkovi zbytečné informace. Kódy chyb odkazují na chyby, které jsou podrobně popsány v tomto článku.

V závislosti na chybě, ke které došlo, obsahuje tabulka v tomto článku následující údaje:

- Popis stavu, který chybu způsobil, nebo další údaje
- Informace ke zvážení v prostředí nebo konfiguracích platebních konektorů
- Informace, na které lze odkazovat v případě podpory, pokud je vyžadována další pomoc

## <a name="checkout-module-error-reference-codes"></a>Referenční kódy chyb modulu pokladny

V následující tabulce získáte další informace o odkazech na chybové kódy, které poskytují zákazníci nebo se zobrazují v internetovém obchodě.

| Kód chyby | Kód chyby korelovaný dynamicky | Popis chyby |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Platbu nebylo možné autorizovat. ID typu karty v **TokenizedPaymentCard** chybí nebo zadané ID typu karty není podporováno. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Zamítnuto. Platbu nebylo možné autorizovat. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Platbu nebylo možné autorizovat. Od zákazníka jsou požadovány další informace. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Omlouváme se, došlo k chybě. Nepodařilo se nám získat výsledek přijetí platby kartou. Zkuste to znovu nebo kontaktujte správce systému. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Nelze provést platbu z důvodu chybějících vlastností platby obchodníka. Obraťte se na správce systému. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Nelze načíst platební službu pro operaci. Zkontrolujte nastavení platební metody pro vybraný typ platby. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Platba z účtu zákazníka již byla použita a je povolena pouze jedna platba na jednu transakci. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Limit zákaznického účtu se liší od dlužné částky. Zkuste jinou platební metodu nebo se obraťte na zákaznickou podporu. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Platba na zákaznický účet převyšuje celkovou splatnou částku za uvedené položky. Zkuste to později nebo požádejte zákaznickou podporu o pomoc. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Platba účtu odběratele vyžaduje vlastní účet nebo odpovídající účet faktury na řádku úhrady. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Momentálně nelze zpracovat platbu z účtu zákazníka - hodnota minimálního limitu byla překročena. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Tento zákazník nemá povoleno platit na účet. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Omlouváme se, došlo k chybě. Platbu nebylo možné zrušit. Zkuste to znovu. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Při zpracování platby došlo k chybě. Zkuste to znovu později. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Částka platby prostřednictvím věrnostní karty překračuje částku povolenou pro tuto věrnostní kartu v rámci této transakce. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Částka refundace prostřednictvím věrnostní karty překračuje částku povolenou pro tuto věrnostní kartu v rámci této transakce. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Číslo věrnostní karty nebylo nalezeno. Číslo věrnostní karty aktivujte nebo zadejte jiné číslo karty a poté opakujte akci. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Číslo věrnostní karty není dostupné. Zadejte jiné číslo karty a zkuste to znovu. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Tato věrnostní karta neumožňuje uplatnit věrnostní body pro tuto transakci. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | U čísla dárkové karty došlo k chybě. Zkuste jinou dárkovou kartu nebo se obraťte na zákaznickou podporu. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Částka přesahuje zůstatek na dárkové kartě. Zadejte jinou částku a zkuste to znovu. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Transakce nemůže obsahovat více než jeden řádek věrnostní platby. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Údaje o platbě buď chybí, nebo jsou nesprávné. Ověřte platební údaje a zkuste to znovu. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Objednávka momentálně nemohla být zpracována. Zkuste to znovu později. |
| CCR025     | Vypršení časového limitu rozhraní frontend pro rozhraní API pokladny | Časový limit operace front-endu vypršel. Potvrďte, zda byla objednávka zpracována v Dynamics 365 Commerce headquarters. |
| CCR026     | Původní autorizovaná částka změněna | Částka objednávky se změnila z původní autorizační částky zpracované platební bránou. Může to být způsobeno časovým vypršením platnosti kupónu, propagační akce nebo prodeje. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Při zpracování platby došlo k chybě. Odkaz poskytnutý na rozhraní API košíku má jiný odkaz, než se očekávalo (s upozorněním na potenciální nekonzistenci během procesu placení). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | U zvolené platební metody došlo k chybě. Chcete-li zkontrolovat nastavení účtu, kontaktujte podporu nebo to zkuste znovu s jinou platební metodou. |

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](dev-itpro/payments-retail.md)

[Modul pokladny](add-checkout-module.md)

[Platební modul](payment-module.md)
