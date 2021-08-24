---
title: Začněte s výpočtem daně
description: Toto téma vysvětluje, jak nastavit výpočet daně.
author: wangchen
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1f75fb48cc9af5513916b509056ee08569e6118c82f7c2f9e86f1db6fae3bafd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769687"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Začínáme s doplňkem výpočtem daně (preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace o tom, jak začít pracovat s výpočtem daně. Nejprve vás provede kroky konfigurace ve službách Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Poté představí běžný proces používání možností výpočtu daně v transakcích Finance a Supply Chain Management.

Nastavení se skládá ze čtyř hlavních kroků:

1. V LCS nainstalujte výpočet daně.
2. V RCS nastavte funkci výpočtu daně. Toto nastavení není specifické pro určitou právnickou osobu. Lze jej sdílet mezi právnickými osobami v aplikacích Finance a Supply Chain Management.
3. Ve Finance a Supply Chain Management nastavte parametry výpočtu daně podle právnické osoby.
4. Ve Finance a Supply Chain Management vytvářejte transakce, jako jsou prodejní objednávky, a pomocí výpočtu daně určujte a vypočítávejte daně.

## <a name="prerequisites"></a>Předpoklady

Než budete moci dokončit postupy uvedené v tomto tématu, musí být splněny následující předpoklady:

- Máte přístup ke svému účtu LCS a nasadili jste projekt LCS s prostředím úrovně 2 (nebo vyšším), ve kterém běží Dynamics 365 verze 10.0.18 s [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) nebo novější.
- Máte přístup k vašemu účtu RCS.
- Kontaktovali jste společnost Microsoft, aby povolila testování ve vašem nasazeném prostředí Finance nebo Supply Chain Management.

## <a name="set-up-tax-calculation-in-lcs"></a>Nastavení výpočtu daně v LCS

1. Přihlaste se do [LCS](https://lcs.dynamics.com)
2. Dokončete nastavení integrace Microsoft Power Platform. Další informace naleznete v tématu [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Vyberte jedno ze svých nasazených neprodukčních prostředí a pak vyberte možnost **Nainstalovat nový doplněk**.
4. Vyberte možnost **Výpočet daně (preview)**.
5. Přečtěte si smluvní podmínky, vyjádřete s nimi souhlas a poté vyberte možnost **Instalovat**.

## <a name="set-up-tax-calculation-in-rcs"></a>Nastavení výpočtu daně v RCS

Kroky v této části nesouvisí s konkrétním právním subjektem. Tento postup musíte dokončit pouze jednou a můžete jej dokončit u jakékoli právnické osoby v RCS.

1. Přihlaste se do [RCS](https://marketing.configure.global.dynamics.com/).
2. Přejděte do pracovního prostoru **Správa funkcí**, vyberte a zapněte funkci **Funkce globalizace**.
3. V pracovním prostoru **Elektronické výkaznictví** přidejte nového poskytovatele konfigurace. Jako název poskytovatele použijte název vaší společnosti. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
4. Vyberte poskytovatele konfigurace, kterého jste právě vytvořili, a pak vyberte možnost **Nastavit jako aktivní**.
5. Vyberte poskytovatele konfigurace **Microsoft** a poté vyberte **Úložiště**.
6. V poli **Typ** vyberte **Globální**.
7. Zvolte **Otevřít**.
8. Přejděte do části **Model daňových dat**, rozbalte strom souborů a poté vyberte možnost **Konfigurace daní**.
9. Vyberte nejnovější verzi a poté vyberte **Importovat**.
10. Vraťte se do pracovního prostoru **Funkce globalizace**, vyberte **Funkce**, vyberte dlaždici **Výpočet daně** a poté vyberte příkaz **Přidat**.
11. Vyberte jeden z následujících typů funkce:

    - **Nová funkce** – Vytvořte nastavení funkce, která má prázdný obsah.
    - **Na základě stávající funkce** – Vytvořte funkci z existující funkce a zkopírujte obsah z nastavení existující funkce.

11. Zadejte název a popis nové funkce a poté vyberte **Vytvořit funkci**.

    Po vytvoření funkce se automaticky vytvoří její koncept.

12. Vyberte konceptovou verzi funkce a poté vyberte příkaz **Upravit**. Stránka **Nastavení výpočtu daně** je vyplněna.
13. Vyberte **Verze konfigurace**. Měla by se zobrazit verze konfigurace, kterou jste importovali v kroku 8.

    Společnost Microsoft poskytuje výchozí konfiguraci daně pro doplněk výpočtu daně. Tato konfigurace pokrývá většinu požadavků na chování výpočtu daně. Bude aktualizován na základě zpětných vazeb trhu. Pokud musíte rozšířit konfiguraci, aby splňovala konkrétní požadavky, v tématu [Jak vytvořit rozšíření v daňové službě](./tax-service-add-data-fields-tax-integration-by-extension.md) najdete informace o tom, jak vygenerovat a vybrat vlastní daňovou konfiguraci.

    Poté, co vyberete **Verzi konfigurace**, objeví se několik dalších karet:

    - **Daňové kódy** – Tato karta je povinná. Používá se k udržování kmenových dat pro daňové kódy. Všechny daňové kódy, které jsou vytvořeny na této kartě, se automaticky synchronizují do Finance, když v právnické osobě povolíte aktuální verzi nastavení funkce daně.
    - **Použitelnost daňových kódů** – Tato karta je povinná. Používá se k definování matice, která určuje kód daně, daňovou skupinu a daňovou skupinu zboží. Stanovený kód daně se používá k výpočtu částky daně. Hodnoty polí **Kód daně**, **Daňová skupina** a **Daňová skupina zboží** jsou vráceny do Finance.
    - **Použitelnost DIČ zákazníka** – Tato karta je volitelná. Pokud máte více daňových registračních čísel pro jednoho zákazníka, může výpočet daně automaticky určit správné daňové registrační číslo. V matici na této kartě definujete pravidla, která se používají k určení DIČ. Jinak budou Finance a Supply Chain Management i nadále používat u prodejních transakcí výchozí daňové registrační číslo na zdanitelných dokladech.
    - **Použitelnost DIČ dodavatele** – Tato karta je volitelná. Pokud máte více daňových registračních čísel pro jednoho dodavatele, může výpočet daně automaticky určit správné daňové registrační číslo. V matici na této kartě definujete pravidla, která se používají k určení DIČ. Jinak budou Finance a Supply Chain Management i nadále používat u nákupních transakcí výchozí daňové registrační číslo na zdanitelných dokladech.
    - **Použitelnost kódu seznamu** – Tato karta je volitelná. Může pomoci automaticky určit hodnotu pole **Kód seznamu** prostřednictvím flexibilnějších a konfigurovatelnějších pravidel. V matici na této kartě definujete pravidla, která se používají k určení DIČ. Jinak budou Finance a Supply Chain Management i nadále používat u zdanitelných dokladů výchozí kód.

14. Na kartě **Daňové kódy** vyberte **Přidat** a zadejte daňový kód a popis.
15. Vyberte možnost **Daňová komponenta**. Daňová komponenta je skupina metod, které byly definovány v předchozí verzi vybrané daňové konfigurace. K dispozici jsou následující daňové komponenty:

    - Podle čisté částky
    - Podle hrubé částky
    - Podle množství
    - Podle marže
    - Daň z daně

16. Zvolte **Uložit**. Na základě vybrané daňové komponenty se zpřístupní více polí.
17. Pomocí následujících možností můžete určit povahu daňového kódu:

    - Je osvobozeno od daně
    - Je importní DPH
    - Je přenesení daňové povinnosti
    - Vyloučit z výpočtu základní částky

    Pro scénář importní DPH nastavte jeden daňový kód, který má kladnou sazbu daně, a označte jej jako **Je importní DPH**.

    Pro scénář přenesení daňové povinnosti nastavte dva daňové kódy, z nichž jeden má kladnou sazbu daně a druhý má zápornou sazbu daně, ale stejnou hodnotu sazby. Označte záporný daňový kód jako **Je přenesení daňové povinnosti**. Další informace o řešení přenesení daňové povinnosti ve Finance najdete v části [Mechanismus přenesení daňové povinnosti pro režim DPH / GST](emea-reverse-charge.md).
    
    U některých typů daní, které by měly být vyloučeny při výpočtu částky základu daně u transakcí zahrnujících cenu, jako je celní sazba v některých zemích, vyberte zaškrtávací políčko **Vyloučit z výpočtu základní částky**.

    Udržujte daňové sazby a limity výše daně pro tento daňový kód.

18. Opakujte kroky 14 až 17 pro všechny další povinné daňové kódy, které chcete přidat.
19. Na kartě **Použitelnost daňových kódů** vyberte sloupce, které jsou nutné k určení správného daňového kódu, a poté vyberte **Přidat**.
20. Zadejte nebo vyberte hodnoty pro každý sloupec. Hodnoty polí **Kód daně**, **Daňová skupina** a **Daňová skupina zboží** budou výstupem z této matice.
21. Opakováním kroků 19 až 20 nastavíte použitelnost DIČ zákazníka, DIČ dodavatele a kódů seznamu.
22. Zvolte **Uložit** a pak zavřete stránku.
23. Vyberte **Změnit stav** \> **Dokončeno**. Po změně stavu na **Dokončeno** již verzi nelze upravovat.
24. Vyberte **Změnit stav** \> **Publikovat**. Tato verze nastavení funkce daně bude přenesena do globálního úložiště a bude viditelná pro každou právnickou osobu ve službě Finance.

## <a name="dynamics-365-setup"></a>Nastavení Dynamics 365

Po dokončení nastavení v RCS, které je popsané v předchozí části, budete mít publikovanou verzi funkce daně. Pomocí těchto kroků nastavíte výpočet daně ve Finance.

Nastavení v této části provádí právnická osoba. Musíte jej konfigurovat pro každou právnickou osobu, pro kterou chcete ve Finance aktivovat výpočet daně.

1. Ve Finance přejděte do nabídky **Daň** \> **Nastavení** \> **Daňová konfigurace** \> **Nastavení výpočtu daně (preview)**.
2. Na kartě **Obecné** natavte následující pole:

    - **Povolit výpočet daně** – Zaškrtnutím tohoto políčka povolíte výpočet daně pro právnickou osobu. Pokud není pro aktuální právnickou osobu povolen, bude právnická osoba i nadále k určení a výpočtu daně používat stávající daňový modul.
    - **Nastavení funkce** – Vyberte publikované nastavení a verzi daňové funkce pro právnickou osobu. Další informace o tom, jak nastavit a dokončit publikovanou daňovou funkci, najdete v předchozí části tohoto tématu.
    - **Obchodní proces** – Vyberte obchodní procesy, které chcete povolit.
    - **Povolit úpravu daňového kódu** – Nastavte tuto možnost na **Ano** a povolte tak úpravy daňového kódu na stránce DPH.

3. Na kartě **Výpočet** definujte očekávané pravidlo zaokrouhlování pro právnickou osobu.
4. Na kartě **Zpracování chyb** definujte očekávanou metodu zpracování chyb pro právnickou osobu. Pro každý kód výsledku jsou k dispozici tři možnosti:

    - Žádný
    - Upozornění
    - Chyba

5. Uložte nastavení.
6. Opakujte kroky 1 až 5 pro každou další právnickou osobu.

## <a name="transaction-processing"></a>Zpracování transakcí

Po dokončení všech postupů nastavení můžete pomocí výpočtu daně určit a vypočítat daň ve službě Finance. Kroky při zpracování transakcí zůstávají stejné. Ve službě Finance verze 10.0.18 jsou podporovány následující transakce:

- Proces prodeje

    - Prodejní nabídka
    - Prodejní objednávka
    - Potvrzení
    - Výdejka
    - Dodací list
    - Prodejní faktura
    - Dobropis
    - Vratka
    - Náklady v záhlaví
    - Náklady řádku

- Proces nákupu

    - Nákupní objednávka
    - Potvrzení
    - Příjemka
    - Příjemka produktu
    - Nákupní faktura
    - Náklady v záhlaví
    - Náklady řádku
    - Dobropis
    - Vratka
    - Nákupní žádanka
    - Poplatky řádku nákupní žádanky
    - Požadavek na nabídku
    - Náklady záhlaví požadavku na nabídku
    - Poplatky řádku požadavku na nabídku

- Proces zásob

    - Převodní příkaz – expedice
    - Převodní příkaz – příjem
