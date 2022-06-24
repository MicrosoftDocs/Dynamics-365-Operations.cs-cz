---
title: Vytvoření a fakturace mezipodnikové prodejní objednávky pro externího odběratele
description: Tento článek vysvětluje postup vytvoření a fakturace mezipodnikové prodejní objednávky pro externího odběratele
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: cd42551730ab0123813a3b5a0b5a4b1c334e9d30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852150"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Vytvoření a fakturace mezipodnikové prodejní objednávky pro externího odběratele

[!include [banner](../../includes/banner.md)]

Mezipodnikový obchod můžete použít pro záznam prodeje produktu od jedné právnické osoby jiné právnické osobě, která se nachází v rámci stejné organizace.

Když vytváříte původní prodejní objednávku, můžete automaticky vytvořit mezipodnikovou nákupní objednávku pro mezipodnikového dodavatele. Tím se automaticky vytvoří mezipodniková prodejní objednávka u právnické osoby mezipodnikového dodavatele.

Následující obrázek znázorňuje tok transakce, když vytvoříte prodejní objednávku pro externího odběratele, ale než bude možné produkt dodat odběrateli, produkt musí být objednán od jiné právnické osoby ve vaší organizaci. V tomto případě je mezipodniková nákupní objednávka vytvořena pro účet dodavatele, který představuje jinou právnickou osobu. Následně se mezipodniková prodejní objednávka vytvoří u jiné právnické osoby pro účet odběratele, který představuje vaší právnickou osobu. Jestliže je mezipodniková nákupní objednávka fakturována a jedná se o přímou dodávku, faktura pro původní prodejní objednávku se automaticky zaúčtuje.

![Mezipodnikový externí prodejní proces](media/intercompanyexternalsalesprocess.png)

Používáte-li přímou dodávku a v poli **Množství** ve stránce **Zaúčtování faktury** vyberete možnost **Dodací list**, bude mezipodniková faktura dodavatele založena na dříve zaúčtované mezipodnikové příjemce produktu.

## <a name="prerequisites"></a>Předpoklady

Před zahájením práce se ujistěte, zda jsou splněny následující předpoklady k automatickému zaúčtování a tisku mezipodnikových faktur.

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Na stránce **Mezipodnikové** pro dodavatele nebo odběratele vyberte v oblasti **Zásady nákupních objednávek** ve skupině polí **Mezipodniková nákupní objednávka (přímá dodávka)** zaškrtávací políčko **Zaúčtovat fakturu automaticky**.
1. V oblasti **Zásady nákupních objednávek** ve skupině polí **Původní prodejní objednávka (přímá dodávka)** vyberte zaškrtávací políčko **Zaúčtovat fakturu automaticky**. Toto políčko zaškrtněte, pokud chcete, aby faktury pro původní prodejní objednávku byly automaticky vytištěny při zaúčtování mezipodnikové faktury dodavatele.

> [!NOTE]
> Nastavení tisku pro fakturu je určeno v nastavení modulu, dokumentu nebo transakce ve stránce **Nastavení správy tisku**.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Vytvoření původní prodejní objednávky pro externího odběratele

Tyto kroky proveďte u právnické osoby A. Tento postup odpovídá políčku 1 na obrázku.

1. Přejděte na **Pohledávky \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Na stránce se seznamem **Všechny prodejní objednávky** vytvořte původní prodejní objednávku. Hodnoty pole se zkopírují z účtu odběratele do prodejní objednávky.
1. V podokně akcí na stránce **Prodejní objednávka** zvolte **Zobrazení záhlaví**.
1. Na záložce **Mezipodniková nastavení** vyberte zaškrtávací políčko **Automaticky vytvářet mezipodnikové objednávky**.
1. Pokud chcete, aby váš mezipodnikový dodavatel dodal položku přímo externímu zákazníkovi, zapněte zaškrtávací políčko **Přímá dodávka**.
1. Po ukončení zadávání prodejní objednávky zavřete stránku **Prodejní objednávka**.

Automaticky se vytvoří mezipodniková nákupní objednávka pro všechny položky s přiřazeným mezipodnikovým dodavatelem, a pak se vytvoří mezipodniková prodejní objednávka. Informační zpráva vám sdělí, že byla vytvořena mezipodniková nákupní objednávka a mezipodniková prodejní objednávka. Zpráva také obsahuje odkazy na tyto objednávky. Pokud nebyla položka nalezena, zobrazí se červené varování, které znamená, že proces vytváření objednávky nebyl dokončen.

> [!NOTE]
> Pokud vytváříte několik objednávek u různých právnických osob a v jedné z právnických osob nebyly položky nalezeny, proces vytváření objednávek se zastaví i pro právnické osoby, které objednávky mohou splnit.

## <a name="invoice-an-intercompany-sales-order"></a>Fakturace mezipodnikové prodejní objednávky

Když se vyfakturuje mezipodniková prodejní objednávka, automaticky se vyfakturuje také odpovídající mezipodniková nákupní objednávka. Pokud původní prodejní objednávka představuje přímou dodávku, originální prodejní objednávka se automaticky vyfakturuje.

Tyto kroky proveďte u právnické osoby B. Tento postup odpovídá políčku 2 na obrázku.

1. Přejděte na **Pohledávky \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Na stránce seznamu **Všechny prodejní objednávky** vyberte mezipodnikovou prodejní objednávku.
1. V části Podokno akcí vyberte kartu **Faktura** a potom vyberte možnost **Faktura**.
1. Zaškrtněte políčko **Zaúčtování**.
1. Vyberte prodejní objednávku a poté vyberte **OK**.

Faktura odběratele pro mezipodnikovou prodejní objednávku je automaticky zaúčtována u právnické osoby B. Mezipodniková faktura dodavatele je pak automaticky vytvořena a zaúčtována u právnické osoby A. Pokud je původní prodejní objednávka nastavena jako přímá dodávka, dojde k vytvoření faktury odběratele pro původní prodejní objednávku u právnické osoby A.

> [!NOTE]
> Dříve v případě scénářů mezipodnikového prodeje platilo, že když byl pracovní postup faktury dodavatele konfigurován v mezipodnikové nákupní společnosti, nebylo možné mezipodnikovou prodejní objednávku úspěšně fakturovat. Proto musel být pracovní postup faktury dodavatele pro mezipodnikovou nákupní společnost vypnut. 
> 
> Toto omezení bylo opraveno nedávnou funkcí ve vydání 10.0.25. Mezipodnikové prodejní objednávky lze nyní fakturovat, když je v mezipodnikové nákupní společnosti konfigurován pracovní postup faktury dodavatele.
> 
> Pokud chcete tuto funkci povolit, postupujte takto.
>
> 1. Zvolte právnickou osobu mezipodnikového prodeje.  
> 2. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
> 3. Vyberte zákazníka pro mezipodnikovou nákupní společnost.
> 4. Přejděte do nabídky **Všeobecné \> Nastavení \> Mezipodnikové**.
> 5. Na kartě **Zásady nákupních objednávek** vyberte parametr **Obejít pracovní postup faktury dodavatele pro mezipodnikové faktury dodavatelů**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
