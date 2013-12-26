Press Release Sculpin Bundle
============================

Quick example of how to add a new type of content to Sculpin. This is a work in
progress (WIP) and should only be used as an example. It is highly likely this
process will no longer be needed for longer than a month or so.


Setup
-----

To enable a custom bundle, add its class name to a custom SculpinKernel in
`app/SculpinKernel.php`. The class should extend `AbstractKernel`.

    class SculpinKernel extends \Sculpin\Bundle\SculpinBundle\HttpKernel\AbstractKernel
    {
        protected function getAdditionalSculpinBundles()
        {
            // Return an array of strings that represent the classes of the
            // Sculpin bundles.
            return array('Reflx\Sculpin\PressBundle\ReflxPressBundle');
        }
    }

Either require your package as an external package in `sculpin.json` or make
sure to configure your autoloader in `sculpin.json` if you intend for your
bundle to live locally.
