---
title: Kupóny
description: Tento článek poskytuje přehled možností souvisejících s kupóny v Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709752"
---
# <a name="coupons"></a>Kupóny

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled možností souvisejících s kupóny v Microsoft Dynamics 365 Commerce.

Kupóny jsou kódy a čárové kódy, které slouží k přidání slev do transakcí. Maloobchodníci distribuují kupóny potenciálním nebo stávajícím zákazníkům, aby jim pomohli zlepšit povědomí o značce, podpořit konverzi, udržet si zákaznickou základnu, zvýšit prodej a případně zvýšit příjmy. Kupony se staly jedním z nejoblíbenějších marketingových nástrojů a jsou novou normou v prodeji přes elektronické obchodování.

V Dynamics 365 Commerce jsou kupony spojeny se slevami a jsou považovány za dodatečné ověření nad rámec slev. Každý kupón se vztahuje k jedné slevě a propojená sleva definuje sadu produktů, na které kupón platí.

Cenové skupiny, které jsou spojeny se slevou, definují způsobilé podmínky, pro které lze kupón použít. Tyto podmínky zahrnují skupiny zákazníků a prodejní kanály. Kupóny také poskytují **Limit použití** a vlastnosti **Zákazníkem vyžadováno**, které lze použít ke konfiguraci volitelných omezení použití.

Každý kupón může mít několik kódů kupónů a čárových kódů kupónů a všechny kódy mohou mít vlastní rozsah dat účinnosti a stav. Pokud je stav kódu nastaven na **Neaktivní**, kód nelze použít v žádném kanálu.

## <a name="set-up-a-coupon"></a>Nastavení kupónu

Před nastavením kupónu je nutné nakonfigurovat čárový kód kupónu a dvě číselné řady kupónu.

Chcete-li nastavit kupón v Commerce headquarters, postupujte podle následujících pokynů.

1. Přejděte na **Retail a Commerce \> Řízení zásob \> Čárové kódy a popisky \> Znaky masky**.
1. Vyberte **Přidat** pro vytvoření znaku masky typu **Kód kupónu**. V poli **Znak** můžete vybrat libovolný nepoužitý znak.
1. Přejděte na **Retail a Commerce \> Řízení zásob \> Čárové kódy a popisky \> Nastavení čárového kódu a masky**.
1. Vyberte **Nový** pro vytvoření masky čárového kódu typu **Kód kupónu**.
1. Přejděte na **Retail a Commerce \> Řízení zásob \> Čárové kódy a popisky \> Nastavení čárového kódu**.
1. Vyberte **Nový** pro vytvoření nového čárového kódu, který používá vytvořenou masku čárového kódu.
1. Přejděte na **Správa organizace \> Číselné řady**.
1. Vytvořte dvě číselné řady:

    1. Jednu řadu pro referenci **Číslo kupónu**. Tato sekvence definuje jedinečný identifikátor kupónu.
    1. Jednu řadu pro referenci **ID kódu kupónu**. Tato sekvence definuje jedinečný identifikátor pro každý kód kupónu pro kupón.

    Pro obě číselné řady je nutné nastavit pole **Obor** na **Společnosti**. Ve většině případů byste měli automaticky generovat obě pořadová čísla.

1. Přejděte do nabídky **Parametry Commerce \> Ceny a slevy \> Kupóny**.
1. Nastavte pole **Maska čárového kódu kupónu** na čárový kód, který jste vytvořili dříve.
1. Přejděte na **Parametry Commerce \> Číselné řady**.
1. Vyberte číselné řady, které jste dříve vytvořili pro reference **Číslo kupónu** a **ID kódu kupónu**.

Chcete-li nastavit kupón, musíte vytvořit slevu a kupón samostatně a poté je propojit výběrem slevy v poli **Sleva** konfigurace kupónu. Poté, co je kupón spojen se slevou, pole **Stav**, **Datum účinnosti** a **Datum ukončení platnosti** propojené slevy se stanou pouze pro čtení, protože hodnoty jsou určeny stavem kuponu a dobou platnosti. Když je stav kupónu nastaven na **Aktivní**, stav propojené slevy se automaticky aktualizuje na **Povolená**. Podobně, když je stav kupónu nastaven na **Nektivní**, stav propojené slevy se automaticky aktualizuje na **Zakázaná**.

## <a name="use-a-coupon"></a>Použití kupónu

Chcete-li přidat kupón na prodejní transakci v pokladním místě (POS) Commerce, můžete použít kód kupónu nebo čárový kód kupónu. Chcete-li použít kód kupónu, vyberte operaci **Přidat kód kupónu** a poté zadejte kód. Pro použití čárového kódu kupónu můžete naskenovat čárový kód pomocí skenovacího zařízení nebo ho zadat pomocí numerické klávesnice na obrazovce **Transakce**.

Obchodníci někdy chtějí, aby pokladní mohli poskytovat zákazníkům slevy v pevné výši z důvodů uklidnění nebo kvůli vadám produktů, ale nechtějí tisknout kódy kuponů a distribuovat je pokladním. V tomto případě můžete nastavit možnost **Použít bez kódu kupónu** pro kupón na **Ano**. Pokladní POS pak mohou používat funkci **Použít kupón** uvnitř operace **Zobrazit dostupné slevy** pro přidání kupónu k transakci bez ručního zadávání kódu. Pokud pro záhlaví kupónu existuje více kódů kupónů, systém automaticky vybere první aktivní kupón a použije ho na transakci.

Chcete-li přidat kupón do prodejní objednávky call centra, musí uživatel call centra vybrat možnost **Kupony** na kartě **Spravovat** v podokně akcí na stránce prodejní objednávky.

Chcete kupující přidat kupón do objednávky elektronického obchodu, může zadat kód kupónu do pole **promo kód** v nákupním košíku.

Po přidání kupónu do prodejní objednávky cenový modul okamžitě spustí přepočet pro celou objednávku bez ohledu na to, zda je povolen zpožděný výpočet.

> [!NOTE]
> Ve verzi Commerce 10.0.30 a starší, poté, co uživatelé call centra přidají kupon do prodejní objednávky call centra, musí vybrat **Přepočítat** ve skupině **Vypočítat** na kartě **Prodat** v podokně akcí, aby mohli uplatnit slevu spojenou s daným kupónem.

## <a name="coupon-usage-limit"></a>Limit použití kupónu

Kupóny lze konfigurovat na omezené použití. Limit použití lze definovat na jednoho zákazníka, na kanál nebo globálně. Limit použití je vynucen na kód kupónu v kupónu. Jednorázový kupón, který má dva kódy, lze například použít dvakrát: jednou pro každý kód.

Kupóny lze použít napříč prodejními kanály. Pro call centrum však lze kupóny s omezeným použitím uplatnit pouze v případě, že je nastavení **Povolit dokončení objednávky** v nastavení kanálu call centra aktivní. Pokud je nastavení **Povolit dokončení objednávky** deaktivováno, lze uplatnit pouze kupóny bez omezeného použití.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
