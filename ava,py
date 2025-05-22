import asyncio
from pyppeteer import launch

async def main():
    browser = await launch(headless=False, args=['--start-maximized'])
    page = await browser.newPage()
    await page.goto('https://faucets.chain.link/', {'waitUntil': 'networkidle2'})

    # Wait for the wallet address input to appear
    await page.waitForSelector('input[type="text"]', timeout=20000)

    # Fill in your Avalanche Fuji testnet wallet address
    wallet_address = '0xYourFujiWalletAddress'  # <-- REPLACE THIS
    await page.type('input[type="text"]', wallet_address)

    # Select Avalanche Fuji (the selector may change, inspect the page if needed)
    # Example: The label might contain "Avalanche Fuji"
    await page.click('label[for="avalancheFuji"]')  # Adjust if selector changes

    # Click the "Send Request" button (adjust selector if needed)
    await page.click('button[type="submit"]')

    # Wait for a few seconds to see the result
    await page.waitFor(5000)

    print("Faucet request sent (if all went well).")
    await browser.close()

asyncio.get_event_loop().run_until_complete(main())
