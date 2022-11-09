---
title: Povolit vyhledávání objednávek pro hostující pokladny
description: Tento článek popisuje, jak povolit vyhledávání objednávek pro hostující pokladny v Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 757e83887e318dd6aa54106fb78305f1d94e0f90
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734237"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Povolit vyhledávání objednávek pro hostující pokladny

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit vyhledávání objednávek pro hostující pokladny v Microsoft Dynamics 365 Commerce.

Vyhledávání objednávek pro hostující pokladny umožňuje zákazníkům, kteří nakupují jako hostující uživatelé, vyhledávat jejich objednávky. Funkce vyhledávání objednávek je užitečná, když zákazníci chtějí provádět akce, jako je kontrola stavu plnění produktů na objednávce, ověření adresy, na kterou byla objednávka odeslána, změna pořadí produktu nebo potvrzení obchodu, ze kterého bude objednávka vyzvednuta.

Zákazníci, kteří zadávají objednávky jako registrovaní uživatelé, mohou vidět podrobnosti o své objednávce, když jsou přihlášeni, ale zákazníci, kteří k zadávání objednávek používají hostující pokladnu, nemohou. Když je však povolena funkce vyhledávání objednávek pro hostující pokladny, poskytuje formulář, který mohou zákazníci použít k vyhledávání objednávek, které zadali jako hosté. Do tohoto formuláře zákazníci zadávají ID potvrzení objednávky a (volitelně) e-mailovou adresu, kterou uvedli při pokladně.

Do transakčních e-mailů souvisejících s objednávkou lze navíc zahrnout odkaz nebo tlačítko, které zákazníka přenese přímo na stránku s podrobnostmi objednávky. Tento odkaz nebo tlačítko bude fungovat pro objednávky, které zadávají registrovaní uživatelé i hostující uživatelé.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Zapněte potřebné funkce v centrále Commerce

Chcete -li povolit vyhledávání objednávek pro hostující pokladny, musíte v adrese zapnout následující funkce **Pracovní prostory \> Správa funkcí** v obchodní centrále.

| Funkce | Účel |
|---------|---------|
| Funkce volby anonymního vyhledávání detailů objednávky uživatele v Retailu | Tato funkce zpřístupňuje uživatelské rozhraní v parametrech Commerce, které vám umožňují povolit API pro vyhledávání objednávek pro neověřené uživatele a konfigurovat způsob zobrazení osobních údajů. |
| Povolit generování silnějšího ID odkazu na kanál | Tato funkce generuje bezpečnější 12znakové ID reference kanálu (ID potvrzení objednávky), které lze předat v řetězci dotazu při vyhledávání objednávky. |
| Generovat konzistentní formát ID referenčního kanálu napříč kanály | Tato funkce generuje ID bezpečného referenčního kanálu pro objednávky zadané prostřednictvím webu elektronického obchodování, maloobchodního prodejního místa (POS) nebo call centra. Než budete moci tuto funkci zapnout, musí být zapnutá funkce **Povolit generování silnějšího referenčního ID kanálu**. |

Poté, co zapnete funkci **Maloobchodní funkce anonymního vyhledávání podrobností vyhledávání uživatelů**, musíte povolit rozhraní API, které podporuje neověřené vyhledávání objednávek v centrále Commerce. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Objednávky zákazníků**. Na stránce **Objednávky zákazníků** na záložce s náhledem **Hledání objednávek** nastavte možnost **Povolit neověřené vyhledávání objednávek** na **Ano**, jak ukazuje následující obrázek.

## <a name="manage-the-display-of-personal-data"></a>Správa zobrazení osobních údajů

Záložka s náhledem **Hledání objednávek** na stránce **Objednávky zákazníků** v centrále Commerce obsahuje pole **Zahrnout osobní údaje do vyhledávání objednávek hostů**, které vám umožňuje řídit, zda se osobní údaje zobrazují zákazníkům. Tyto osobní údaje zahrnují dodací adresu zákazníka a poslední čtyři číslice čísla kreditní karty zákazníka. Ve výchozím nastavení se osobní údaje zákazníkům nezobrazují, pokud je povoleno vyhledávání neověřených objednávek. V následující tabulce jsou popsány dostupné možnosti.

| Parametr | Výsledek |
|--------|--------|
| Nikdy | Výchozí hodnota Při vyhledávání objednávek se nezobrazují žádné osobní údaje. Když registrovaní uživatelé, kteří jsou přihlášeni, vyhledají objednávku, kterou vytvořili, když byli přihlášeni, uvidí své osobní údaje. |
| Pouze objednávky hostů | Osobní údaje se zobrazují při ve vyhledávacích kódech objednávek, které zákazníci vytvořili jako hosté. Pokud byla objednávka vytvořena registrovaným uživatelem, musí se tento uživatel přihlásit, aby viděl jeho osobní údaje. |
| Všechny objednávky | Při všech vyhledáváních objednávek se zobrazují všechny osobní údaje. |

> [!NOTE]
> Tyto možnosti určují, kdy se anonymní hostující uživatelé zobrazí osobní údaje, jako je adresa zákazníka a poslední čtyři číslice čísla kreditní karty zákazníka. V zájmu ochrany soukromí registrovaných zákazníků doporučujeme vybrat volbu **Pouze objednávky hostů**. Nejbezpečnější možností však je **Nikdy**.

Poté, co změníte hodnotu pole **Zahrnout osobní údaje do vyhledávání objednávek hostů**, musíte spustit úlohu 1070 (**Konfigurace kanálu**) v centrále Commerce tím, že přejdete na **Retail a Commerce \> Retail a Commerce IT \> Plán distribuce**.

## <a name="configure-the-order-lookup-module"></a>Konfigurace modulu pro vyhledávání objednávek

Modul vyhledávání objednávek v knihovně modulů Commerce se používá k vykreslení formuláře, který hostující uživatelé používají k vyhledávání objednávek. Modul pro vyhledávání objednávek lze zahrnout do hlavního slotu jakékoli stránky, která nevyžaduje přihlášení zákazníka. Informace o konfiguraci modulu najdete v části [Vyhledávací modul objednávky](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Konfigurace stránky s podrobnostmi objednávky

Než si uživatelé typu host budou moci zobrazit podrobnosti o své objednávce, musí být stránka s podrobnostmi objednávky na vašem webu elektronického obchodu nakonfigurována tak, aby nevyžadovala přihlášení. Chcete-li vypnout požadavek na přihlášení pro stránku s podrobnostmi o objednávce, otevřete stránku v konfigurátoru webů Commerce a vyberte slot **Výchozí stránka (povinné)** ve stromovém zobrazení a vymažte zaškrtávací políčko **Vyžaduje přihlášení?** ve spodní části podokna vlastností vpravo.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Přidání odkazu na podrobnosti objednávky v transakčních e-mailech

V e-mailech souvisejících s objednávkou můžete uvést odkaz nebo tlačítko, které zákazníky přesměruje na stránku s podrobnostmi o objednávce. Chcete-li přidat tento odkaz nebo tlačítko, vytvořte hypertextový odkaz HTML, který odkazuje na stránku s podrobnostmi objednávky na vašem webu elektronického obchodu, a předejte ID potvrzení objednávky a e-mailovou adresu zákazníka jako parametry adresy URL, jak je znázorněno v následujícím příkladu.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

> [!NOTE]
> Chcete-li povolit funkci vyhledávání objednávek, ujistěte se, že je klíč **Nabídka** je povolen v části **Konfigurace licence** > **Konfigurační klíče**.
>
>![Musí být povolena konfigurace licenčního klíče nabídek](./media/Quotations_License_Key_Configuration.png)

## <a name="additional-resources"></a>Další prostředky

[Modul vyhledávání objednávky](order-lookup-module.md)

[Nastavení profilu oznámení e-mailem](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
