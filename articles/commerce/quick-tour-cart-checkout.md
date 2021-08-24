---
title: Přehled stránek košíku a pokladny
description: Toto téma poskytuje přehled stránek košíku a pokladny v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8b983ac7f25d629e532769a331a9880b24f3745a195f2c0e9752b238039232a0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763708"
---
# <a name="cart-and-checkout-pages-overview"></a>Přehled stránek košíku a pokladny

[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled stránek košíku a pokladny v řešení Microsoft Dynamics 365 Commerce.

Stránka košík na webu e-Commerce zobrazuje všechny položky, které odběratel přidal do nákupního košíku. Stránka vozíku je sestavena pomocí modulu košík. Modul košíku je kontejner, který hostuje všech modulů, které jsou nutné k prezentaci položek v nákupním košíku. Modul vozík může rovněž použít jiné moduly, které zobrazují souhrn objednávek a všechny kódy speciální nabídky, které byly použity pro objednávku odběratele.

Stránka rezervace na webu e-Commerce představuje krok za krokem, podle kterého se zákazníci budou řídit zadáním všech informací, které jsou požadovány pro uvedení objednávky. Modul poklady může obsahovat moduly, které zpracovávají dodací adresu, způsob dopravy, fakturační informace, souhrn objednávky a další informace, které souvisejí s objednávkami zákazníka.

## <a name="cart-page"></a>Stránka košíku

Stránka košíku slouží jako nákupní sáček a zahrnuje všechny položky, které byly přidány do nákupního košíku.

Následující ilustrace znázorňuje příklad stránky košíku, která byla sestavena pomocí knihovny modulů a tématu "Fabrikam".

![Příklad stránky košíku.](./media/cart2.PNG)

HLavní část stránky košíku zobrazuje všechny položky, které odběratel přidal do nákupního košíku. Přednastaveny všechny použitelné slevy. Tyto slevy zahrnují složité slevy. Příklady zahrnují "nákup 3 položky a získej 10% slevu" nebo "kup láhev a batoh a získej slevu 10%." V modulu souhrn objednávek je zobrazena částka, která je splatná po použití slev, expedice, daní atd. Existuje také modul propagačního kódu, který umožňuje odběrateli použití nebo odebrání propagačních kódů.

Odběratel může nakupovat anonymně nebo jako přihlášený uživatel. Pokud je odběratel přihlášen, položky v nákupním košíku zůstanou mezi relacemi zachovány. Tímto způsobem může zákazník pokračovat v nakupování z více zařízení.

Z nákupního košíku může odběratel přejít k pokladně. Zákazník může zahájit rezervaci jako uživatel typu Host nebo jako přihlášený uživatel.

Informace o tom, jak vytvořit stránku nákupního košíku, naleznete v tématu [Přidání modulu košíku na stránku](add-cart-module.md).

## <a name="checkout-page"></a>Stránka pokladny

Na stránce pokladny jsou umístěny informace vyžadované k zadání objednávky.

Následující ilustrace znázorňuje příklad stránky pokladny, která byla sestavena pomocí knihovny modulů.

![Příklad stránky pokladny.](./media/Checkout.PNG)

Hlavní část stránky pokladny, v níž jsou shromážděny všechny informace o objednávce. Tyto informace zahrnují dodací adresu, možnosti dodání a informace o platbě. Pokladna má tok krok za krokem, protože informace musí být zadány v určitém pořadí, které má být zpracováno. Před vypočítáním nákladů na dodání je například nutné zadat dodací adresu a autorizovat platbu.

### <a name="shipping-address"></a>Dodací adresa

Pokud musí být zboží expedováno, je požadováno dodání adresy. Formát adres pro dodání jednotlivých národních prostředí lze konfigurovat v aplikaci Dynamics 365 Commerce. Pokud budou například položky expedovány do Spojených států, musí doručovací adresa obsahovat ulici, stát a PSČ. Některé základní ověření vstupu se provádí pro pole adresy expedice, jako je například ověření alfanumerických znaků, maximální délka a počet. Ačkoli platnost samotné adresy není ověřena, toto ověření lze provést pomocí přizpůsobených služeb třetích stran.

Dodací adresa je použita pro všechny položky v vozíku, pro který je vybrána možnost "expedice". Pokud používáte tok rezervace, který je poskytován v knihovně modulů, jednotlivé položky nákupního košíku nelze odeslat na jiné adresy. Pokud tuto funkci požadujete, lze ji implementovat pomocí vlastního nastavení modulů rezervace.

Po dodání adresy expedice jsou zobrazeny metody expedice, které jsou k dispozici v online obchodu Dynamics 365 Commerce. Způsoby expedice a adresy, které podporují, lze konfigurovat v aplikaci Commerce.

### <a name="payment"></a>Platba

Dalším krokem v toku pokladny je platba. V e-Commerce lze k umísťování objednávek, jako jsou kreditní karty, dárkové poukazy a věrnostní body, použít více způsobů platby. Lze také použít kombinaci těchto způsobů platby. V závislosti na použitých metodách plateb mohou být vyžadovány další informace. Například platba kreditní kartou vyžaduje fakturační adresu. Platby kreditních karet jsou zpracovávány pomocí konektoru platby Adyen.

#### <a name="loyalty-points"></a>Věrnostní body

Během toku pokladny může odběratel, který je členem věrnostního programu a který má časově rozlišené věrnostní body, vyplatit tyto věrnostní body pro objednávku. Modul věrnostní body se zobrazí pouze v případě, že odběratel má existující věrnostní členství. Pro uživatele, kteří nejsou členy a uživatelé typu Host, je tento modul skrytý.

#### <a name="gift-cards"></a>Dárkové poukazy

Knihovna modulů umožňuje, aby byly pro objednávku uplatněny interní dárkové poukazy. Chcete-li použít interní dárkový poukaz, je nutné, aby byl zákazník přihlášen. Pro zvýšení zabezpečení doporučujeme tok přizpůsobit pomocí osobního identifikačního čísla (PIN) pro interní dárkové poukazy.

### <a name="signed-in-and-guest-users"></a>Přihlášení a uživatelé typu Host

Zákazník může dokončit proces pokladny jako uživatel typu Host nebo jako přihlášený uživatel. Pokud se zákazník přihlásí v aplikaci, budou automaticky načteny informace o účtech, jako jsou například uložené přepravné adresy a uložené podrobnosti platební karty.

### <a name="order-summary"></a>Souhrn objednávky

Položka rezervace zobrazí souhrn položek řádku v vozíku, takže zákazník může ověřit objednávku dříve, než ji zadá. Položky řádku nelze upravit v průběhu postupu pokladny. Odkaz na košík je však uveden v případě, že uživatel chce přejít zpět a upravit položky řádku.

Poté, co odběratel poskytne informace o dodávce a fakturaci, zobrazí souhrn objednávky částku, která je splatná po uplatnění věrnostních bodů, dárkových poukazů a dalších plateb.

### <a name="order-confirmation-and-email"></a>E-mail a potvrzení objednávky

Když odběratel zadá objednávku, je zadáno číslo potvrzení. V tomto okamžiku byla platba autorizována, ale nebyla zaúčtovaná. Platba bude účtována pouze v případě, že je objednávka splněna (tj. byla expedována nebo vyzvednuta).

Po vytvoření objednávky je odběrateli odeslán e-mail s potvrzením objednávky.

Další informace o tom, jak vytvořit stránku pokladny, naleznete v tématu [Přidání modulu pokladny na stránku](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled domovské stránky](quick-tour-home-page.md)

[Přehled stránek s podrobnostmi o produktu](quick-tour-pdp.md)

[Přehled stránek správy účtů](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
