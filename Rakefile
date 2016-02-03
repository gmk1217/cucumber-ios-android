def run_tests(deviceName, platformName, platformVersion, app)
  system("deviceName=\"#{deviceName}\" platformName=\"#{platformName}\" platformVersion=\"#{platformVersion}\" app=\"#{app}\" parallel_cucumber features -n 20")
end

task :Galaxy_S5_Device do
  run_tests('Samsung Galaxy S5 Device', 'Android', '4.4', 'http://saucelabs.com/example_files/ContactManager.apk')
end

task :Galaxy_S4_Emulator do
  run_tests('Samsung Galaxy S4 Emulator', 'Android', '4.4', 'http://saucelabs.com/example_files/ContactManager.apk')
end

task :iPhone_5_Simulator do
  run_tests('iPhone 5', 'iOS', '8.4', 'https://s3.amazonaws.com/appium/TestApp8.4.app.zip', 'junit_reports/iPhone_6_Simulator')
end

task :iPhone_6_Simulator do
  run ('iPhone 6', 'iOS', '8.4', 'https://s3.amazonaws.com/appium/TestApp8.4.app.zip', 'junit_reports/iPhone_6_Simulator')
end

multitask :run_feature => [
  :Galaxy_S5_Device,
  :Galaxy_S4_Emulator,
  :iPhone_5_Simulator,
  :iPhone_6_Simulator

] do
  puts 'Running automation'
end
