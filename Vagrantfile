Vagrant.configure("2") do |config|

  config.vm.define :nginx do |nginx|
    nginx.vm.box = "debian/bullseye64"
    nginx.vm.hostname = "nginx"
    nginx.vm.synced_folder ".", "/vagrant", disabled: true
    nginx.vm.network :public_network,
      :dev => "br0",
      :mode => "bridge",
      :type => "bridge",
      use_dhcp_assigned_default_route: true
  end
end
